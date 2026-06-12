# How to Replace the Nozzle

Replacing the nozzle is a common maintenance task, whether due to a clog you can't clear, wear and tear, or to switch to a different diameter (e.g., from 0.4mm to 0.6mm for faster prints).

!!! danger "Severe Burn Hazard"
    This procedure involves very high temperatures (up to 285°C). The nozzle and heater block can cause severe and instantaneous burns.
    Handle with extreme care and consider wearing heat-resistant gloves. The thermistor and heater wires are also very fragile.

---

### Tools and Preparation

!!! info "Tools Needed :wrench:"
    * **New Nozzle:** Make sure you have the correct replacement nozzle.
    * **17mm Wrench:** Or an adjustable wrench, to hold the heater block.
    * **7mm Socket Wrench:** Or needle-nose pliers, to unscrew/tighten the nozzle.

### Step-by-Step Procedure

1.  **Access the Nozzle**
    On the printer's menu, move the Z-axis as high as possible to get good working access to the hotend.

2.  **Heat the Nozzle :thermometer:**
    On the menu, go to `Settings -> Temperature -> Nozzle` and set the temperature to **285°C**.

    !!! note "Why 285°C?"
        Heating the nozzle is **essential**. The heat expands the metal, which allows you to:
        -   Remove the old nozzle without damaging the threads.
        -   Ensure the new nozzle seals perfectly to prevent future leaks of molten plastic.

3.  **Unload the Filament**
    If any filament is loaded, run the "Unload Filament" routine on your printer.

4.  **Remove the Old Nozzle**

    !!! warning "Critical Step: Hold the Heater Block!"
        Use the 17mm wrench to **firmly** hold the heater block while you unscrew the nozzle. If you fail to do this, you risk twisting and breaking the "heatbreak" (the thin tube connecting the block to the heatsink), which would result in a much more complex repair.

    With the block secured, use the 7mm wrench to unscrew and remove the old nozzle. Remember it is extremely hot.

5.  **Install and Tighten the New Nozzle :sparkles:**
    -   Keeping the temperature at 285°C, carefully screw in the new nozzle by hand as far as it will go.
    -   While again holding the heater block with the 17mm wrench, use the 7mm wrench to give it the **final tightening**. It should be snug, but do not overtighten.

    !!! tip "A Small Gap is Normal"
        When the nozzle is fully tightened, it is normal for a small gap to exist between the hexagonal head of the nozzle and the heater block. Do not try to tighten further to close this gap.

### Finalization

!!! success "Mandatory Calibration"
    Whenever you replace the nozzle, the distance to the print bed will change slightly. It is **highly recommended** (nearly mandatory) to re-run the **"First Layer Calibration"** to ensure perfect adhesion and prevent the new nozzle from crashing into the bed.