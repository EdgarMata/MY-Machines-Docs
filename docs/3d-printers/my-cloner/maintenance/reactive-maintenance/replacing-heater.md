# How to Replace the Hotend Heater Cartridge

The heater cartridge is the metal cylinder responsible for heating the hotend block. If your printer fails to reach the target temperature or shows a "Preheat Failure" error, the heater may be faulty.

!!! danger "Safety Warning: Disconnect the Printer :electric_plug:"
    Always unplug the printer from the power outlet before starting any work on the electronics. Ensure the hotend is completely cool.

---

### General Replacement Procedure

1.  **Disconnect from Mainboard**
    Open the electronics case. Locate the extruder heater wires (usually the thickest wires coming from the hotend) and disconnect them from the mainboard.

2.  **Release the Heater from the Block :wrench:**
    -   On the heater block, locate the small screw (usually a grub screw) that clamps the heater cartridge in place.
    -   Use the correct Allen key to loosen it enough for the cartridge to slide out.

3.  **Remove the Old Heater**
    Pull the old cartridge out of the heater block. It might require a bit of wiggling if it's a tight fit.

4.  **Install the New Heater :sparkles:**
    -   Slide the new heater cartridge into the block, making sure it is fully inserted.
    -   Tighten the retaining screw. It should be snug to ensure good thermal contact, but do not overtighten to the point of deforming the cartridge.

    !!! tip "Good Thermal Contact is Essential"
        A securely fastened screw ensures that heat is transferred efficiently from the heater to the block, leading to more stable temperature readings.

5.  **Connect to Mainboard**
    Route the new wires and connect them to the correct port on the mainboard.

### Finalization and Calibrations

!!! success "Mandatory Calibrations :arrows_counterclockwise:"
    Just like with the thermistor, replacing the heater changes the heating dynamics of the system.
    * **PID Calibration:** It is mandatory to run a new PID calibration.
    * **Thermal Model Calibration (if applicable):** This safety calibration should also be re-run for the new component.