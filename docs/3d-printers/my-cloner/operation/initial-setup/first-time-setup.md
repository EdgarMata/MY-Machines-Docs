# First Time Setup & Calibration Guide

Before your first print, you must perform a series of essential one-time calibrations. This process ensures the printer knows its physical limits and is tuned for accurate, reliable printing.

!!! warning "Complete This Guide First"
    Do not attempt to print a model before completing every step in this guide. Skipping these calibrations can result in failed prints or even damage to the printer.

---
### Step 1: Homing the Printer

"Homing" is the process where the printer moves each axis until it touches its endstop switch. This allows Klipper to establish a known zero position (0,0,0).

1.  Turn on your printer and connect to the Klipper web interface.
2.  In the control panel, click the "Home All" button (often an icon of a house).
3.  The printer will move the X, Y, and then Z axes until they each trigger their endstop.

### Step 2: PID Tuning (Hotend & Bed)

PID tuning calibrates the heating algorithm to ensure temperatures are stable and do not overshoot or fluctuate. This is critical for print quality.

1.  In the console, run the PID tune command for the hotend. A common target temperature for PLA is 215°C.
    ```bash
    PID_CALIBRATE HEATER=extruder TARGET=215
    ```
2.  Wait for the process to complete. [cite_start]It will run through several cycles of heating and cooling. [cite: 566]
3.  Once finished, type `SAVE_CONFIG` in the console and press enter. This saves the new PID values to your `printer.cfg`.
4.  Repeat the process for the heatbed. A common target for PLA is 60°C.
    ```bash
    PID_CALIBRATE HEATER=heater_bed TARGET=60
    ```
5.  When it finishes, run `SAVE_CONFIG` again.

### Step 3: Calibrating Probe Z-Offset

This is the most important calibration for getting a perfect first layer. It measures the exact vertical distance between your probe's trigger point and the tip of the nozzle.

1.  Home the printer with `G28`.
2.  Move the nozzle to the center of the bed.
3.  In the console, run the command: `PROBE_CALIBRATE`
4.  The printer will now enter the calibration tool. Place a single sheet of standard office paper under the nozzle.
5.  Use the `TESTZ Z=-` and `TESTZ Z=+` commands to lower and raise the nozzle in very small increments. Lower the nozzle until you feel slight friction on the paper as you move it back and forth.
6.  Once you feel the friction, run the `ACCEPT` command.
7.  Finally, run `SAVE_CONFIG` to store the Z-offset permanently.

### Step 4: Building the Bed Mesh

This process uses the probe to measure a grid of points across your print bed, creating a digital map of its surface to compensate for any slight warping.

1.  Ensure the printer is homed and the nozzle is hot (to account for any thermal expansion).
2.  In the console, run the command: `BED_MESH_CALIBRATE`
3.  The printer will now automatically probe multiple points on the bed.
4.  When it's finished, run `SAVE_CONFIG` to store the mesh data.

!!! success "Setup Complete!"
    Your printer is now calibrated. The final step is to start your first print and fine-tune the first layer live, as the `PROBE_CALIBRATE` value can sometimes need minor adjustments. While the first layer is printing, use the Z-Offset controls in the web interface to get that perfect "squish." 