# Software, Slicer, and Firmware Issues

!!! abstract "The Problem"
    Sometimes the printer's hardware is working perfectly, but the print still fails. These issues stem from the software toolchain: the 3D model (STL), the slicer that generates the G-code, or the firmware running on the printer itself.

<figure markdown="1">
  ![The 3D printing software toolchain](../../images/image-placeholder.png#only-light){ width="600" }
  ![The 3D printing software toolchain](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>An illustration of the software toolchain in 3D printing, including the 3D model, the slicer software, and the G-code file sent to the printer.</figcaption>
</figure>

## Common Problems and Solutions

### Problem: A print fails at the exact same height or spot every time.

* **Cause:** This is a classic symptom of a corrupted G-code file or a flaw in the 3D model itself. The error is "baked into" the instructions, so the printer faithfully repeats the mistake every time.
* **Solution:**
    1.  **Re-slice the Model:** The simplest fix is to open the original STL file in your slicer and slice it again. Save it with a new filename to a different SD card if possible. This often resolves corruption that occurred during the first slicing or saving process.
    2.  **Try a Different Slicer:** To rule out a bug in your slicer software, try slicing the model with an alternative program (e.g., if you use Cura, try PrusaSlicer, or vice versa). If it prints correctly, you know the issue was with the original slicer's settings or version.
    3.  **Repair the 3D Model:** The original STL file might be faulty (e.g., have non-manifold edges or holes). Open the model in a 3D viewer and inspect it for errors. Use a tool like Windows 3D Builder or Meshmixer to run an automatic repair function on the model before slicing.

### Problem: The printer's screen is frozen, blank, or shows garbage characters.

* **Cause:** This usually indicates a firmware crash or corruption. It can be triggered by a faulty command from a bad G-code file or an issue during the printer's boot-up sequence.
* **Solution:**
    1.  **Power Cycle:** The first step is always to turn the printer off, wait 30 seconds, and turn it back on.
    2.  **Remove SD Card:** A corrupt SD card can sometimes prevent the printer from booting correctly. Remove the card and restart the printer. If it boots normally, the card is the problem.
    3.  **Re-flash Firmware:** This is the definitive solution. Download the correct, official firmware for your specific printer model and mainboard version. Follow the manufacturer's instructions to re-install (or "flash") the firmware.

### Problem: Slicer settings are not affecting the print.

* **Cause:** Some printers store their own configuration settings in an internal memory called EEPROM. These stored settings (e.g., for acceleration or jerk) can override the commands sent from the slicer's G-code.
* **Solution:**
    * **Check Start G-code:** Look in your slicer's machine settings for the "Start G-code" section. See if there are any commands like `M201`, `M204`, or `M205` that might be setting these values at the start of every print.
    * **Reset EEPROM (Advanced):** You can connect to your printer with a terminal like Pronterface or OctoPrint and send the command `M502` to reset the settings to the firmware defaults, followed by `M500` to save those defaults. **Warning:** This will erase any calibrations you have saved, like Z-offset and PID tunes.

## Quick Checklist
- [ ] If a print fails repeatedly at the same spot, re-slice the model.
- [ ] Try using a different slicer to rule out software bugs.
- [ ] Inspect and repair the original STL model for errors.
- [ ] If the screen is frozen, try restarting without the SD card.
- [ ] As a last resort for screen/boot issues, re-flash the printer's firmware.