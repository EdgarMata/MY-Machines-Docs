# How to Replace the Hotend Assembly

Replacing the entire hotend assembly may be necessary in case of severe damage, such as a broken heatbreak or damaged wires that cannot be repaired individually.

!!! danger "Safety Warning: Disconnect the Printer :electric_plug:"
    Before you begin, always disconnect the printer from the power outlet. This operation involves disconnecting sensitive electronic components and handling internal wiring.

!!! note "This is a General Guide"
    The exact steps may vary depending on your printer's specific design. Please consult your "MY Cloner" assembly manual for precise details on how to disassemble the extruder carriage.

---

### General Replacement Procedure

1.  **Access the Hotend and Electronics**
    You may need to remove the fan shroud or other parts of the extruder carriage to get full access to the hotend. Also, open the electronics case to access the mainboard.

2.  **Disconnect Cables at the Mainboard**
    -   Locate the cables for the **heater** and **thermistor** from the extruder.
    -   Take a photo of the connections before unplugging them so you have a reference for reassembly.
    -   Carefully disconnect them from the mainboard.

3.  **Remove the Old Hotend :wrench:**
    -   The hotend is typically held in place on the extruder body by one or two screws. Unscrew them.
    -   Carefully remove the old hotend assembly, pulling its cables through the existing path.

4.  **Install the New Hotend :sparkles:**
    -   Position the new hotend correctly and tighten the mounting screws.
    -   Route the new heater and thermistor cables along the same path as the old ones.
    -   Connect them to the correct ports on the mainboard, using your photo as a reference.
    -   Re-mount any fans or shrouds you removed.

### Finalization and Calibrations

!!! success "Mandatory Post-Replacement Calibrations :arrows_counterclockwise:"
    Whenever you replace critical hotend components, you **must** re-run certain calibrations to ensure the printer's safety and performance.
    * **PID Calibration:** This tunes the heating algorithm for the new hardware. Look for this option in the printer's menu.
    * **Thermal Model Calibration (if applicable):** Newer printers use this for safety. It must be re-run.
    * **First Layer Calibration:** The Z-height (nozzle-to-bed distance) will have changed, so this calibration is essential.