# How to Replace the Hotend Thermistor

The thermistor is the small sensor that measures the temperature of the heater block. If your printer shows erratic temperatures or a "MINTEMP" / "MAXTEMP" error, the thermistor or its cable is likely damaged.

!!! danger "Safety Warning: Extremely Fragile Component :warning:"
    The thermistor's wires are **very thin and fragile**. The glass or metal bulb at the tip is also delicate. Handle with extreme care to avoid damage. Always unplug the printer from the power source before you begin.

---

### Replacement Procedure

1.  **Cool Down the Hotend**
    Ensure the hotend is completely cool to the touch.

2.  **Disconnect from Mainboard :electric_plug:**
    Open the electronics case, locate the extruder thermistor connector on the mainboard, and carefully disconnect it.

3.  **Remove from Heater Block :wrench:**
    -   The thermistor is a small cartridge inserted into a hole in the heater block, typically held in place by a small screw on its side.
    -   Use the appropriate Allen key to **loosen this screw very slightly**. The goal is not to remove the screw, just to relieve the pressure.
    -   Gently pull the old thermistor out of the block. If it's stuck, do not force it. Heating the block slightly might help loosen any plastic residue holding it.

4.  **Install the New Thermistor :sparkles:**
    -   Insert the new thermistor into the hole until it is fully seated.
    -   **Very carefully** tighten the retaining screw. The goal is only to secure it in place, not to crush it. **If you overtighten, you will damage the new thermistor.**

5.  **Connect to Mainboard**
    Route the new cable and plug it into the correct port on the mainboard.

### Finalization and Calibrations

!!! success "Mandatory Calibrations :arrows_counterclockwise:"
    Whenever the thermistor is changed, the hotend's thermal behavior changes.
    * **PID Calibration:** You must run a new PID calibration so the printer can learn how to maintain a stable temperature with the new sensor.
    * **Thermal Model Calibration (if applicable):** This safety calibration must also be re-run.