# Klipper Interface Guide

The My-Cloner uses **Mainsail** as its main control interface.

Mainsail runs in a web browser and allows you to control, monitor and configure the printer through the Raspberry Pi Zero 2 W.

This page introduces the main areas of the interface and the controls you will use most often.

---

## Accessing Mainsail

Make sure the My-Cloner is powered on and that the Raspberry Pi Zero 2 W has completed its startup process.

From a computer, tablet or phone connected to the same network, open the My-Cloner Mainsail address in a web browser.

When the connection is successful, Mainsail should show the printer status as:

**Klipper Ready**

If Klipper reports an error, resolve the error before attempting to move or heat the printer.

---

## Main Dashboard

The Mainsail dashboard provides an overview of the current printer status.

The most important areas are:

- Printer status
- Temperature controls
- Movement controls
- Extruder controls
- G-code files
- Console
- Print status

<figure markdown="1">
  ![Mainsail Dashboard](/assets/images/image-placeholder.webp#only-light){ width="700" }
  ![Mainsail Dashboard](/assets/images/image-placeholder.webp#only-dark){ width="700" }
  <figcaption>Typical Mainsail dashboard layout.</figcaption>
</figure>

---

## Printer Status

The printer status area shows the current Klipper state.

Typical states include:

- Ready
- Printing
- Paused
- Complete
- Error
- Shutdown

Under normal conditions, the printer should show:

**Ready**

If an error is displayed, read the message carefully before continuing.

---

## Temperature Controls

The temperature section displays the current and target temperatures for the main heaters.

For the My-Cloner, this normally includes:

- Extruder
- Heated bed

The temperature graph helps you monitor:

- Current temperature
- Target temperature
- Heating stability
- Cooling behaviour

You can also set heater temperatures manually from this section.

!!! warning "Check Temperature Readings First"
    Before activating any heater, make sure the reported temperatures are realistic.

    Do not heat the printer if a sensor reports an invalid or unexpected value.

---

## Movement Controls

The movement controls allow manual positioning of the printer axes.

The My-Cloner uses:

- X — extruder left/right
- Y — bed forwards/backwards
- Z — gantry up/down

You can normally choose movement increments such as:

- 0.1 mm
- 1 mm
- 10 mm
- 50 mm

!!! warning "Home Before Large Movements"
    Do not command large axis movements before the printer has been homed.

    Klipper needs a known machine position before normal movement can be considered safe.

---

## Homing Controls

Mainsail provides controls for homing the printer.

The My-Cloner uses:

- X endstop for X homing
- Y endstop for Y homing
- P.I.N.D.A. probe as part of the Z homing system

A complete homing cycle can also be started from the console with:

    G28

Only perform homing after completing the sensor and movement checks in the [First Time Setup & Calibration](first-time-setup.md) guide.

---

## Extruder Controls

The extruder controls allow you to feed or retract filament.

Typical controls include:

- Extrude
- Retract
- Extrusion length
- Extrusion speed

The hotend must be above the minimum extrusion temperature before Klipper allows extrusion.

!!! warning "Do Not Extrude Cold Filament"
    Never force filament through a cold hotend.

    Heat the nozzle to the correct temperature for the material before using the extruder controls.

For normal filament handling, follow:

[How to Load and Unload Filament](loading-unloading-filament.md)

---

## Fan Controls

Mainsail allows control of fans that are configured as controllable outputs in Klipper.

Depending on the configuration, you may be able to control:

- Part-cooling fan
- Additional configured fans

The hotend cooling fan may operate automatically according to temperature.

---

## G-Code Files

The G-code files section contains the files available for printing.

You can normally:

- Upload files
- View file information
- Delete files
- Start a print

G-code should be generated using the recommended **My-Cloner OrcaSlicer profile**.

Do not use a G-code file created for a different printer unless you have verified all machine settings.

---

## Uploading a Print File

To upload a G-code file:

1. Slice the model in OrcaSlicer.
2. Export the G-code file.
3. Open Mainsail.
4. Upload the file to the G-code files section.
5. Check the file information before starting the print.

Do not start your first print until the initial calibration procedure has been completed.

---

## Starting a Print

Before starting a print:

- Check that the print surface is clean.
- Make sure the spring steel sheet is installed correctly.
- Confirm that filament is loaded.
- Check that the nozzle is clean.
- Make sure no objects are inside the printer's movement area.
- Confirm that Klipper reports no errors.

Select the G-code file and start the print.

Remain near the printer during the first layer.

---

## Print Status

During a print, Mainsail displays information such as:

- Current layer
- Print progress
- Elapsed time
- Estimated remaining time
- Hotend temperature
- Bed temperature
- Fan speed
- Printer position

Use this information to monitor the print.

---

## Pause, Resume and Cancel

Mainsail provides controls to manage an active print.

### Pause

Temporarily stops the printing process.

Use this when the printer needs attention but the print may still be recoverable.

### Resume

Continues a paused print.

Before resuming, make sure the print can continue safely.

### Cancel

Stops the current print.

Cancel the print if:

- The first layer fails
- The model detaches from the bed
- Filament stops extruding
- A mechanical problem occurs
- Continuing could damage the printer or print

---

## Console

The console provides direct communication with Klipper.

It can be used to:

- Send G-code commands
- Run Klipper calibration commands
- Check printer status
- View errors and responses

Common commands include:

    G28

Home the printer.

    BED_MESH_CALIBRATE

Create a bed mesh.

    PROBE_CALIBRATE

Calibrate the Z probe offset.

    SAVE_CONFIG

Save calibration values to the Klipper configuration.

!!! note
    Only run commands you understand.

    Incorrect movement, heater or configuration commands can cause unexpected printer behaviour.

---

## Emergency Stop

Mainsail provides an emergency stop function.

Use it if the printer behaves unexpectedly and immediate software shutdown is required.

However, if you observe:

- Smoke
- Sparks
- Electrical smell
- Uncontrolled heating
- Serious mechanical collision

use the physical power switch and disconnect the printer from mains power.

---

## Notifications and Errors

Klipper provides detailed error messages when something goes wrong.

Common categories include:

- MCU communication errors
- Temperature sensor errors
- Heater errors
- Homing errors
- Probe errors
- Movement limit errors

Do not repeatedly restart the printer without understanding the cause of an error.

Use the error message as the starting point for troubleshooting.

---

## Recommended Daily Workflow

A typical My-Cloner workflow is:

1. Power on the printer.
2. Open Mainsail.
3. Confirm Klipper is ready.
4. Check temperature readings.
5. Home the printer.
6. Check the print surface.
7. Load filament if required.
8. Upload the G-code file.
9. Start the print.
10. Observe the first layer.
11. Monitor the print from Mainsail.

---

## Next Steps

If you have not yet completed the initial machine calibration, return to:

[First Time Setup & Calibration](first-time-setup.md)

To learn how to change filament:

[How to Load and Unload Filament](loading-unloading-filament.md)

For slicer configuration:

[Setting Up OrcaSlicer](../../software/setting-up-orca-slicer.md)