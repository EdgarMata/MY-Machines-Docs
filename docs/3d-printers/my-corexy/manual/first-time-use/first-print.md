# Your First Print

This is the moment all your hard work has led to. The goal of the first print is not perfection, but a successful test of the entire system working together. We will print a simple calibration cube.

### Step 1: Homing and Bed Leveling

1.  **Homing**: From the web interface, click the "Home All" button (`G28`). Watch all axes carefully as they move to their home positions. Be ready to trigger the emergency stop (or cut power) if anything appears to be crashing.
2.  **Z-Offset Calibration**: This is the process of setting the exact distance between the nozzle and the build plate. Follow the standard Klipper procedure using the `PROBE_CALIBRATE` command. This involves lowering the nozzle until a piece of paper barely grips between the nozzle and the bed.
3.  **Bed Mesh**: Once the Z-offset is roughly set, run a `BED_MESH_CALIBRATE` cycle. This will use the probe to measure the flatness of your bed and create a compensation mesh.
4.  **Save Configuration**: After the mesh is complete, type `SAVE_CONFIG` in the console and press Enter to save your Z-offset and bed mesh.

<figure markdown="1">
  ![Bed mesh visualization in the web interface](/images/image-placeholder.png#only-light){ width="600" }
  ![Bed mesh visualization in the web interface](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A 3D visualization of the bed mesh in the web interface, showing the high and low points of the build surface.</figcaption>
</figure>

### Step 2: Slicing the Calibration Cube

1.  Download a standard 20mm calibration cube STL file from a source like Thingiverse or Printables.
2.  In your slicer, use a basic PLA profile with conservative (slow) speed settings, around 40-50 mm/s. Don't worry about advanced tuning yet.
3.  Slice the model and upload the resulting G-code file to your printer via the web interface.

### Step 3: Starting the Print

1.  Preheat the hotend and bed to your PLA's recommended temperatures.
2.  Start the print.

!!! info "Watch the First Layer Like a Hawk"
    The first layer is the most important part of any print. Watch it closely as it goes down.
    * The extruded lines should be slightly "squished" onto the bed.
    * The lines should be neatly touching each other with no gaps.
    * If the nozzle is too high, the lines won't stick. If it's too low, the filament might look transparent or the extruder might click.
    * Use the "Babystepping" feature in the web interface to make micro-adjustments to the Z-offset *while the first layer is printing* to get it perfect.

<figure markdown="1">
  ![Close-up of a perfect first layer](/images/image-placeholder.png#only-light){ width="700" }
  ![Close-up of a perfect first layer](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>A macro shot of a perfect first layer being printed, showing clean, uniform, and well-adhered lines.</figcaption>
</figure>

### Step 4: Evaluating Your Print

Once the print is finished, let the bed cool down before removing the cube.

Inspect your print. It won't be perfect, and that's okay! The goal was to have a complete object without any catastrophic failures like layer shifts or a "spaghetti" monster. This cube is your baseline. It's the starting point for the real tuning process (like Input Shaper and Pressure Advance) which will elevate your print quality from "successful" to "beautiful."

<figure markdown="1">
  ![The finished calibration cube](/images/image-placeholder.png#only-light){ width="500" }
  ![The finished calibration cube](/images/image-placeholder.png#only-dark){ width="500" }
  <figcaption>A photo of the completed first calibration cube, looking like a recognizable cube.</figcaption>
</figure>

**Congratulations! You've officially built a working 3D printer!**