# Multi-Color Printing on a Single Extruder

You don't need a complex multi-material unit to create prints with multiple colors. By using a simple command in your slicer, you can program the printer to pause at a specific height, allowing you to manually change the filament.

!!! info "How it Works"
    This technique inserts a pause command (`M600` for traditional firmwares, or a `PAUSE` macro in Klipper) into the G-code file at a designated layer. When the printer reaches this command, it will pause the print, move the print head aside, and wait for you to swap the filament before resuming.

---
### How to Set Up a Color Change

1.  **Slice Your Model:** First, slice your model with your normal print settings.
2.  **Find the Target Layer:** In the slicer's preview window, move the layer slider up and down to find the exact layer where you want the color change to occur. Note the layer number or height.
3.  **Add the Color Change Command:** Most modern slicers have a simple feature for this.
    * In **PrusaSlicer** or **SuperSlicer**, you can right-click the "+" icon on the layer slider and select "Add color change (M600)".
    * In **Cura**, you can go to `Extensions -> Post Processing -> Modify G-Code` and add a "Pause at Height" script.
4.  **Configure for Klipper (if needed):**
    * For this to work seamlessly with Klipper, you need to have a set of `PAUSE`, `RESUME`, `UNLOAD_FILAMENT`, and `LOAD_FILAMENT` macros defined in your `printer.cfg`. Many default Klipper configurations come with these pre-configured. Often, a specific `[gcode_macro M600]` is created to run this entire sequence.

### The Printing Process

When the printer pauses for the color change, it will typically:
1.  Stop moving and retract the filament.
2.  Lift the Z-axis and move the print head away from the print.
3.  Beep or wait for you to run an "Unload Filament" command.
4.  Prompt you to insert the new filament and run a "Load Filament" command.
5.  Purge the new filament until the color is pure.
6.  Return to the original position and resume printing with the new color.

<figure markdown="1">
  ![Multi-Color Print](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Multi-Color Print](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>Illustration of a print with a distinct color change at a certain layer, like a logo with two colors.</figcaption>
</figure>
