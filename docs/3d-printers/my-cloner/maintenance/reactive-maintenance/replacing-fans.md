# How to Replace the Fans

The fans are critical for print quality and reliability. If one fails (becomes very noisy or stops spinning), it must be replaced.

!!! danger "Safety Warning: Disconnect the Printer :electric_plug:"
    Always unplug the printer from the power outlet before handling electronic components.

---

### Identifying the Correct Fan

Your printer has two fans on the extruder carriage:

* **Part Cooling Fan:** Usually in the front, it blows air onto the part you are printing. It is crucial for overhang quality and fine details.
* **Hotend Fan:** Usually on the side, it blows air across the hotend's heatsink to prevent heat from traveling upwards and causing clogs ("heat creep").

### Replacement Procedure

1.  **Disconnect the Cable :wrench:**
    Trace the fan's cable to the mainboard and disconnect it. Take note of the port it was plugged into. An electronics diagram can help you identify the ports for the **part cooling fan** and the **hotend fan**.

2.  **Remove the Old Fan**
    Unscrew the bolts holding the fan to the extruder body and remove it.

3.  **Install the New Fan :sparkles:**
    Screw the new fan into the same position.

    !!! tip "Check the Airflow Direction :💨"
        Fans have small arrows on their housing that indicate the direction of airflow. Ensure the new fan is blowing in the correct direction.

4.  **Connect the New Cable**
    Route the new cable along the same path as the old one and plug it into the correct port on the mainboard.

5.  **Test the Functionality**
    Plug in and turn on the printer. Use the settings menu to turn on the fan and confirm that it is spinning freely.

    !!! note "RPM Sensing System"
        Some printers monitor the fan's RPM. If you install an incompatible fan or connect it incorrectly, the printer may display an error on startup.