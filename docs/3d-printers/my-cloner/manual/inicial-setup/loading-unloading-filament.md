# How to Load and Unload Filament

Loading and unloading filament is one of the most common tasks you'll perform with your 3D printer. Following these simple steps will ensure a smooth process and help prevent jams.

---
### How to Load Filament

1.  **Preheat the Nozzle**
    * In the Klipper web interface, go to the Temperature Control section and set the hotend temperature to the correct value for your filament (e.g., 215°C for PLA).
    * Wait for the nozzle to reach the target temperature.

2.  **Prepare the Filament Tip**
    * Take the end of your filament spool and use a pair of snips to cut the tip at a sharp 45-degree angle. This pointy tip makes it much easier to guide the filament into the extruder.

    <figure markdown="1">
      ![Cutting Filament Tip](/images/image-placeholder.png#only-light){ width="600" }
      ![Cutting Filament Tip](/images/image-placeholder.png#only-dark){ width="600" }
      <figcaption>Illustration showing the end of a filament being cut at a 45-degree angle.</figcaption>
    </figure>

3.  **Insert the Filament**
    * Gently guide the pointed end of the filament into the opening at the top of your extruder assembly.
    * Push it in until you feel some resistance, which means it has reached the drive gears.

4.  **Extrude Using the Interface**
    * In the web interface's control panel, click the **"Extrude"** button. The extruder gears will now grab the filament and begin feeding it into the hotend.
    * Keep clicking "Extrude" until you see the new plastic coming out of the nozzle tip. Ensure the flow is smooth and the color is consistent (if you are changing colors).

---
### How to Unload Filament

1.  **Preheat the Nozzle**
    * Just like with loading, you must heat the nozzle to the filament's printing temperature to allow it to be removed. Set the temperature in the web interface.

2.  **Retract the Filament**
    * Once the nozzle is hot, go to the control panel in the web interface and click the **"Retract"** button.
    * The extruder motor will reverse and push the filament back out of the top of the extruder.
    * Gently pull the filament completely out of the printer.