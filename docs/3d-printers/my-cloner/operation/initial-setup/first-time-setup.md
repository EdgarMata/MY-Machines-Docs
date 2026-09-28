# First Time Setup & Calibration

This guide covers the initial motion checks, homing and calibration procedures required before the first print on the **My-Cloner Rev A**.

Before continuing, complete:

- [Before First Power-On](before-first-power-on.md)
- [First Power-On](first-power-on.md)

!!! warning "Complete the Previous Checks First"
    Do not continue if the printer has unresolved electrical, temperature, communication or sensor errors.

---

## 1. Check Stepper Communication and Direction

Before automatic homing, validate each motor independently.

Because an unhomed Klipper axis may reject normal position moves, use the controlled bring-up procedure defined by the current firmware configuration rather than forcing large manual moves.

First confirm that Klipper can communicate with each TMC2209 driver.

The Rev A driver mapping is:

| Function | Driver Position | Klipper Section |
|---|---|---|
| X | X | `stepper_x` |
| Y | Y | `stepper_y` |
| Left Z | Z | `stepper_z` |
| Right Z | E1 | `stepper_z1` |
| Extruder | E0 | `extruder` |

Where appropriate, Klipper's `STEPPER_BUZZ` command can be used during controlled bring-up to confirm that the intended motor responds without requiring a full homing cycle.

Example:

    STEPPER_BUZZ STEPPER=stepper_x

Test one motor at a time.

### X-Axis

Confirm that:

- Only the X motor responds.
- The carriage moves freely.
- The motor direction agrees with the intended machine coordinate system.
- There is no binding, belt skipping or unexpected noise.

### Y-Axis

Confirm that:

- Only the Y motor responds.
- The bed moves freely.
- The direction agrees with the intended machine coordinate system.
- There is no binding, belt skipping or unexpected noise.

### Z-Axis

Test the Left Z and Right Z motors independently before normal Z operation.

Confirm that:

- The Z driver operates the Left Z motor.
- The E1 driver operates the Right Z motor.
- Both motors raise/lower the gantry in the same physical direction when operated together.
- Neither side binds.

!!! warning "Stop If a Motor Moves Incorrectly"
    If a motor moves in the wrong direction or an unexpected motor responds, stop immediately.

    Correct the Rev A Klipper configuration or motor wiring before continuing.

---

## 2. Validate X/Y Sensorless Homing and the P.I.N.D.A.

The My-Cloner Rev A does **not** use physical X or Y endstop switches.

X and Y use **TMC2209 sensorless homing** through StallGuard / DIAG.

Before attempting X or Y homing:

1. Confirm TMC2209 UART communication.
2. Confirm the correct DIAG routing:
   - X → `PA15`
   - Y → `PD2`
3. Configure conservative motor-current values suitable for initial testing.
4. Configure the sensorless-homing parameters in Klipper.
5. Confirm the intended homing direction.
6. Make sure the axis moves freely by hand with power removed.
7. Start with a conservative homing speed and StallGuard threshold.
8. Keep the power switch accessible during the first test.

The P.I.N.D.A. is validated separately for Z.

Confirm that:

- The probe is mounted securely.
- Klipper can read the probe input.
- Its state changes reliably when the probe is actuated by the appropriate test target.
- The final input pin matches the validated Rev A wiring.

!!! danger "Do Not Home with an Unverified Reference System"
    Do not perform automatic homing if TMC2209 UART/DIAG communication or the P.I.N.D.A. input is not behaving as expected.

---

## 3. Home and Tune the X and Y Axes

Test X and Y separately before running a complete `G28`.

For each axis:

1. Position the moving assembly away from the mechanical end with power removed.
2. Restore power and confirm Klipper is ready.
3. Start the individual homing operation.
4. Watch the entire movement.
5. Stop immediately if the axis moves in the wrong direction or pushes continuously against the frame.
6. Adjust `driver_SGTHRS`, motor current or homing speed only as required.
7. Repeat the homing cycle several times.
8. Confirm that the reference position is repeatable.

Check that:

- X moves toward its intended homing end.
- Y moves toward its intended homing end.
- StallGuard stops each axis reliably at the mechanical reference.
- Neither axis false-triggers before reaching the reference.
- Neither motor continues driving against the frame.
- Belts do not slip or skip.

!!! important "Sensorless Homing Is a Physical Calibration"
    A working pin map alone does not validate sensorless homing.

    Final StallGuard thresholds, motor currents and homing speeds must be accepted only after repeated physical tests.

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
- [ ] X TMC2209 UART / DIAG and sensorless homing verified.
- [ ] Y TMC2209 UART / DIAG and sensorless homing verified.
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