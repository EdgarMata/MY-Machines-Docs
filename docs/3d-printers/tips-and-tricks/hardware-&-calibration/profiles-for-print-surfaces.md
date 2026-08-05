# Using Profiles for Different Print Surfaces

If you frequently switch between different print surfaces (e.g., a smooth sheet for PLA and a textured sheet for PETG), you know that each one requires a slightly different Z-offset to get a perfect first layer. Re-calibrating this every time is tedious.

!!! success "The Trick: Save Your Z-Offset in Klipper"
    With Klipper, you can create simple macros to save and recall the exact Z-offset for each of your print sheets, saving you a huge amount of time.

---
### How to Set It Up

This guide assumes you are comfortable editing your `printer.cfg` file.

1.  **Calibrate for Your First Sheet (e.g., Smooth)**
    * Attach your smooth print sheet to the bed.
    * Go through the `PROBE_CALIBRATE` process to find the perfect Z-offset for this sheet.
    * After you `ACCEPT` the value, run `SAVE_CONFIG` in the console. This value is now your printer's baseline.

2.  **Calibrate for Your Second Sheet (e.g., Textured)**
    * Swap to your textured sheet.
    * Heat the printer up and start a first layer calibration print.
    * Use the `SET_GCODE_OFFSET Z_ADJUST=` command to fine-tune the first layer live. For example, if you need to move the nozzle 0.45mm lower for the textured sheet, you would use `SET_GCODE_OFFSET Z_ADJUST=-0.45`.
    * Once the first layer is perfect, note the adjustment value you used.

3.  **Create Macros in `printer.cfg`**
    * Add the following macros to your `printer.cfg` file. These macros will apply the offset and save it.

    ```ini
    [gcode_macro SET_SHEET_SMOOTH]
    gcode:
        SET_GCODE_OFFSET Z=0
        SAVE_CONFIG

    [gcode_macro SET_SHEET_TEXTURED]
    gcode:
        SET_GCODE_OFFSET Z=-0.45  # <-- Replace with your value!
        SAVE_CONFIG
    ```

### How to Use It

Now, when you want to switch print sheets, you just need to run the corresponding command in the console before starting your print:

* For the smooth sheet: `SET_SHEET_SMOOTH`
* For the textured sheet: `SET_SHEET_TEXTURED`

The printer will apply the correct offset and save it, so it persists even after a restart.