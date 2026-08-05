# Understanding the Klipper Web Interface

Your printer runs Klipper firmware, which means you control it through a powerful web interface like **Mainsail** or **Fluidd**. This interface is your primary control center for all printing operations. This guide covers the main sections.

<figure markdown="1">
  ![Klipper Web Interface Dashboard](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Klipper Web Interface Dashboard](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>An overview of a typical Klipper web interface (Mainsail shown).</figcaption>
</figure>

---
### Main Dashboard Sections

* **Temperature Graphs:** This is one of the most important sections. It shows the real-time and target temperatures for your hotend (`extruder`) and `heater_bed`. You can use this to monitor if the printer is heating up correctly and maintaining a stable temperature during printing.
* **Console:** This is a direct command line to your printer. You can type in G-code commands (like `G28` to home) and Klipper commands (like `PID_CALIBRATE`). The console also displays important status updates and error messages.
* **Temperature Control:** This area allows you to manually set target temperatures for your hotend and bed. You can preheat the printer from here before starting a print.
* **Axis Controls:** These buttons allow you to perform basic machine movements.
    * **Homing:** Buttons to home all axes (`Home All`) or individual axes.
    * **Movement:** Buttons to move the X, Y, and Z axes by set amounts. **Note:** You must home the printer before these buttons will work.
* **G-Code Files:** This panel shows a list of all the `.gcode` files you have uploaded to the printer. This is where you will select a file to print.
* **Extruder Controls:** Here you can control the extruder motor to load (`Extrude`) or unload (`Retract`) filament. The hotend must be heated to the material's printing temperature before these controls will work.

---
### How to Start a Print

1.  **Upload G-Code:** Drag and drop your sliced `.gcode` file into the "G-Code Files" panel.
2.  **Preheat (Optional but Recommended):** Manually set the hotend and bed temperatures and wait for them to stabilize.
3.  **Select and Print:** Click on the file you just uploaded and then click the "Print" button. 

