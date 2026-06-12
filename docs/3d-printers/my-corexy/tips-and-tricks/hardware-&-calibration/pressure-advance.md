# Calibrating Pressure Advance

Pressure Advance (PA) is a Klipper firmware feature that compensates for the pressure dynamics inside the hotend's meltzone. When the toolhead slows down for a corner, filament pressure can cause a small blob or bulge to form. PA counteracts this by reducing the extrusion slightly before the corner. It's the key to achieving perfectly sharp corners on your prints.

### The Calibration Method: Pattern Test

The best way to tune Pressure Advance is by printing a special calibration pattern, usually a tall square tower with sharp corners.

1.  **Download the Test Model**: You can find appropriate models in Klipper's official documentation or by searching for "Pressure Advance Tower" on sites like Printables.
2.  **Slice the Model**:
    * Use **0% infill** and **2 perimeters**.
    * Set a reasonably high speed and acceleration to make the effects more obvious (e.g., 100mm/s speed, 3000mm/s² accel).
    * **Crucially, disable any "Jerk Control," "Acceleration Control," or "Wipe" settings in your slicer.** We want Klipper to have full control.
3.  **Prepare the Tuning Command**: Before starting the print, you need to tell Klipper to vary the PA value as the tower prints. In the console, enter the command for your direct-drive extruder:
    `TUNING_TOWER COMMAND=SET_PRESSURE_ADVANCE PARAMETER=ADVANCE START=0 FACTOR=.005`
4.  **Print the Tower**: Start printing the sliced test model immediately after running the command.

### Evaluating the Result

The printed tower will show a clear transition.
* **At the bottom** (low PA), the corners will be rounded and bulging.
* **In the middle**, the corners will become progressively sharper and cleaner.
* **At the top** (high PA), the corners will begin to look starved or have gaps, as the PA is too aggressive.

Your goal is to find the height where the corner quality is best—perfectly sharp, but not yet showing gaps.

<figure markdown="1">
  ![A Pressure Advance calibration tower with measurements](../../images/image-placeholder.png#only-light){ width="600" }
  ![A Pressure Advance calibration tower with measurements](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A Pressure Advance test tower with a pair of digital calipers measuring the height from the bottom of the print to the point with the sharpest, cleanest corners.</figcaption>
</figure>

### Setting Your Final Value

1.  Use digital calipers to precisely measure the height (in mm) from the bottom of the print to the location of the best-looking corners.
2.  Calculate your final Pressure Advance value using the formula:
    `pressure_advance = START + (measured_height * FACTOR)`
3.  Using our example command, if the best height was **45.5mm**, the calculation would be:
    `pressure_advance = 0 + (45.5 * 0.005) = 0.2275`
4.  Open your `printer.cfg` file, find the `[extruder]` section, and add your calculated value:
    `pressure_advance: 0.2275`
5.  Save the configuration and restart Klipper. Your printer will now use this value for all subsequent prints.