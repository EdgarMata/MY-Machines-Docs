# First Time Setup & Calibration

This guide covers the initial motion checks, homing and calibration procedures required before the first print on the **My-Cloner Rev A**.

Before continuing, complete:

- [Before First Power-On](before-first-power-on.md)
- [First Power-On](first-power-on.md)

!!! warning "Complete the Previous Checks First"
    Do not continue if the printer has unresolved electrical, temperature, communication or sensor errors.

---

## 1. Check Axis Movement Direction

Before running automatic homing, verify that each axis moves in the expected direction.

Use the Mainsail controls to move each axis only a small distance.

Start with small movements such as:

- 1 mm
- 5 mm

Check each axis individually.

### X-Axis

The X-axis controls the extruder carriage.

Verify that:

- Positive X movement moves the extruder to the right.
- Negative X movement moves the extruder to the left.

---

### Y-Axis

The Y-axis controls the heated bed.

Verify that the movement direction matches the current Klipper configuration and machine coordinate system.

Use only small movements during this test.

---

### Z-Axis

The Z-axis moves the X-axis gantry vertically.

Verify that:

- Positive Z movement raises the gantry.
- Negative Z movement lowers the gantry.

Both Z motors should move together and remain synchronized.

!!! warning "Stop If an Axis Moves Incorrectly"
    If an axis moves in the wrong direction, stop immediately.

    Correct the motor direction in the Klipper configuration before continuing.

---

## 2. Check Endstops and Probe

Before automatic homing, verify that Klipper can correctly detect the machine reference sensors.

Check the status of:

- X endstop
- Y endstop
- P.I.N.D.A. probe

Use the Klipper console or Mainsail diagnostics to verify that each input changes state when activated.

!!! danger "Do Not Home with an Incorrect Sensor State"
    If an endstop or probe does not respond correctly, do not perform automatic homing.

    A failed sensor can cause the printer to move beyond its mechanical limits.

---

## 3. Home the X and Y Axes

Once the X and Y movement directions and endstops have been verified, home the horizontal axes.

Use the configured homing controls in Mainsail or the Klipper console.

The printer should move each axis toward its configured reference position and stop when the corresponding endstop is triggered.

Observe the complete process.

Check that:

- X moves in the correct homing direction.
- Y moves in the correct homing direction.
- Both axes stop correctly.
- No belt slips or skips.
- No motor continues driving after the endstop is triggered.

---

## 4. Prepare for Z Homing

The My-Cloner uses the **P.I.N.D.A. probe** as part of the Z-axis reference system.

Before Z homing:

- Make sure the spring steel sheet is correctly installed.
- Make sure the print surface is clean.
- Confirm that the P.I.N.D.A. probe is securely mounted.
- Confirm that the probe responds correctly.
- Check that the nozzle is clean.
- Make sure no object is between the nozzle and the bed.

!!! warning "Watch the First Z Homing Carefully"
    Keep your hand near the power switch during the first Z homing procedure.

    If the nozzle approaches the bed without the probe triggering, switch off the printer immediately.

---

## 5. Home the Z-Axis

Run the configured Z homing procedure.

Observe the movement carefully.

The gantry should move toward the bed until the P.I.N.D.A. probe detects the print surface.

Confirm that:

- Both Z motors move correctly.
- The gantry remains approximately level.
- The probe triggers before the nozzle contacts the print surface.
- Klipper completes Z homing without an error.

If the nozzle contacts the bed, stop immediately and correct the probe position or configuration.

---

## 6. Home All Axes

Once individual axis checks have been completed successfully, run a complete homing cycle.

In the Klipper console:

    G28

Observe the full sequence.

The printer should complete homing without:

- Mechanical collisions
- Belt skipping
- Motor stalls
- Endstop errors
- Probe errors

---

## 7. PID Tune the Hotend

PID tuning calibrates the hotend temperature control.

For a typical PLA operating temperature, run:

    PID_CALIBRATE HEATER=extruder TARGET=215

Wait for Klipper to complete the calibration process.

When finished, save the result:

    SAVE_CONFIG

!!! note
    The calibration temperature can be adjusted later if your most commonly used material requires a significantly different printing temperature.

---

## 8. PID Tune the Heated Bed

Run the heated bed PID calibration.

For a typical PLA bed temperature:

    PID_CALIBRATE HEATER=heater_bed TARGET=60

Wait for the procedure to complete.

Then run:

    SAVE_CONFIG

---

## 9. Calibrate the Probe Z Offset

The Z offset defines the vertical distance between the P.I.N.D.A. trigger point and the nozzle tip.

This value is critical for a correct first layer.

Home the printer:

    G28

Then start the probe calibration:

    PROBE_CALIBRATE

Follow the Klipper calibration procedure.

Use a clean sheet of normal office paper between the nozzle and print surface.

Lower the nozzle gradually using the available `TESTZ` commands until you feel light friction when moving the paper.

When the position is correct:

    ACCEPT

Then save the result:

    SAVE_CONFIG

!!! warning "Avoid Bed Damage"
    Make small adjustments when the nozzle approaches the print surface.

    Never force the nozzle against the PEI sheet.

---

## 10. Create the Bed Mesh

Bed mesh calibration measures variations across the print surface and allows Klipper to compensate for them during printing.

Make sure:

- The spring steel sheet is installed.
- The print surface is clean.
- The nozzle is clean.
- The printer is homed.

Run:

    BED_MESH_CALIBRATE

The probe will measure multiple points across the print area.

When the procedure finishes, save the configuration:

    SAVE_CONFIG

---

## 11. Check Extruder Operation

Before loading filament, verify that the extruder motor responds correctly.

Heat the hotend to a safe extrusion temperature before commanding extrusion.

For PLA, approximately:

**200–215 °C**

Use the Mainsail extruder controls to command a small extrusion movement.

Confirm that:

- The motor rotates.
- The drive gears rotate in the correct direction.
- There are no unusual noises.
- The extruder does not skip or bind.

!!! warning "Cold Extrusion"
    Klipper prevents normal extrusion below the configured minimum extrusion temperature.

    Do not disable this protection for normal setup.

---

## 12. Load Filament

Once the extruder has been verified, load filament.

Follow:

[How to Load and Unload Filament](loading-unloading-filament.md)

After loading, extrude a small amount of material and confirm that molten filament exits the nozzle smoothly.

---

## 13. Verify Filament Sensor

If the filament sensor is enabled in Klipper, verify its operation with filament loaded.

Confirm that Mainsail correctly reports the filament state when filament is:

- Inserted
- Removed

Correct the sensor configuration before relying on filament runout detection during printing.

---

## 14. Final Calibration Check

Before the first print, confirm:

- X-axis homes correctly.
- Y-axis homes correctly.
- Z-axis homes correctly.
- P.I.N.D.A. probe operates correctly.
- Z offset has been calibrated.
- Bed mesh has been created.
- Hotend PID calibration is complete.
- Heated bed PID calibration is complete.
- Extruder operates correctly.
- Filament can be loaded and extruded.
- Filament sensor operates correctly, if enabled.
- No Klipper errors are present.

---

## Initial Setup Checklist

- [ ] X-axis direction verified.
- [ ] Y-axis direction verified.
- [ ] Z-axis direction verified.
- [ ] X endstop verified.
- [ ] Y endstop verified.
- [ ] P.I.N.D.A. probe verified.
- [ ] X and Y homing completed successfully.
- [ ] Z homing completed successfully.
- [ ] Full homing completed successfully.
- [ ] Hotend PID tuning completed.
- [ ] Heated bed PID tuning completed.
- [ ] Probe Z offset calibrated.
- [ ] Bed mesh calibrated.
- [ ] Extruder operation verified.
- [ ] Filament loaded successfully.
- [ ] Filament sensor verified, if enabled.
- [ ] Configuration saved with `SAVE_CONFIG`.

---

!!! success "Initial Setup Complete"
    The My-Cloner is now ready for the first test print.

Before printing, make sure OrcaSlicer is configured with the correct My-Cloner profile.

Continue with the software setup and slicing guide:

[Setting Up OrcaSlicer](../../software/setting-up-orca-slicer.md)