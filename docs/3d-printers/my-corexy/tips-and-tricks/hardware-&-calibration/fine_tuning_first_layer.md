# Fine-Tuning The First Layer (Z-Offset)

The main "Perfect First Layer" guide provides an overview, but this page details the step-by-step calibration methods to achieve a flawless foundation for your prints. A perfect Z-Offset is arguably the most critical calibration for print success.

### Method 1: The Paper Test (`PROBE_CALIBRATE`)

This standard Klipper procedure is the best way to establish a solid baseline for your Z-Offset.

1.  Home the printer by pressing the "Home All" button (`G28`).
2.  Move the nozzle to the direct center of the build plate.
3.  Place a single, standard piece of office paper (which is about 0.1mm thick) under the nozzle.
4.  Navigate to the "Console" tab in your web interface and type `PROBE_CALIBRATE`. This will start the interactive calibration tool.
5.  The tool allows you to move the nozzle in tiny increments. Use the `TESTZ` command. For example:
    * `TESTZ Z=-0.1` will move the nozzle down by 0.1mm.
    * `TESTZ Z=0.1` will move the nozzle up by 0.1mm.
    * You can use smaller values like `0.01` for finer control.
6.  Continue sending `TESTZ` commands to lower the nozzle until you feel a slight drag on the paper as you slide it back and forth. The paper should not be pinned tightly, but you should feel definite friction.
7.  Once you achieve the perfect amount of drag, type `ACCEPT` in the console.
8.  **Crucially**, type `SAVE_CONFIG` and press enter. This will save the new offset to your `printer.cfg` and restart the firmware.

<figure markdown="1">
  ![Performing the paper test for Z-Offset calibration](/images/image-placeholder.png#only-light){ width="700" }
  ![Performing the paper test for Z-Offset calibration](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>A hand sliding a piece of paper back and forth under the nozzle during the `PROBE_CALIBRATE` routine to feel for the correct amount of friction.</figcaption>
</figure>

### Method 2: The Live Test (Babystepping)

The paper test gets you close, but the ultimate test is to see the plastic on the plate. Live-tuning during a first layer test print is the best way to achieve perfection.

1.  Find or create a large, single-layer test model (e.g., a 75mm x 75mm square, one layer high).
2.  Slice this model and start the print.
3.  As the first layer is being printed, observe it closely. In your web interface (Mainsail or Fluidd), locate the "Babystep Z" buttons.
4.  Use these buttons to make micro-adjustments to the Z-height, moving it up or down in tiny 0.01mm or 0.05mm increments.
5.  Your goal is to see perfectly "squished" lines of filament that are fused together with no gaps, creating a smooth, glassy surface.
6.  Once the print is finished, note the final Z-offset value displayed in the interface. You can then permanently apply this adjustment in your `printer.cfg` file and run `SAVE_CONFIG` again.

<figure markdown="1">
  ![A close-up macro shot of a perfect first layer](/images/image-placeholder.png#only-light){ width="800" }
  ![A close-up macro shot of a perfect first layer](/images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>A close-up macro shot of a perfect first layer being printed, showing clean, uniform, and well-adhered lines with no gaps.</figcaption>
</figure>