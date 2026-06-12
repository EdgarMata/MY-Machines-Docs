# How to Reduce or Eliminate Stringing

"Stringing," sometimes called "spider webs," is one of the most common and frustrating problems in 3D printing. Fortunately, with the right adjustments, it is almost always possible to eliminate it.

!!! abstract "What is Stringing?"
    Stringing occurs when small strands of plastic are left on a part as the print head moves over open areas. The root cause is filament oozing from the hot nozzle during travel moves, where there should be no extrusion.

![Stringing Example](https://i.imgur.com/cw1aK2g.jpg)

### 1. The Main Culprit: Retraction Settings

Retraction is the function that "pulls" the filament back into the hotend before a travel move. The goal is to relieve pressure in the nozzle to prevent filament from oozing.

* **Retraction Distance:** The amount of filament (in mm) that is pulled back.
    * **Direct Drive Extruders:** The filament path is short. Start with low values: **0.5mm to 2.0mm**.
    * **Bowden Extruders:** The path is long and has some slack. Requires higher distances: **4.0mm to 6.0mm**. Excessive distances can cause clogs.

* **Retraction Speed:** How quickly the filament is pulled back.
    * A speed between **25mm/s and 45mm/s** is a good starting point. If too slow, it won't create a vacuum in time. If too fast, it can grind the filament.

!!! success "Test with a Retraction Tower"
    The best way to find your ideal values is to print a **retraction tower**. This small model tests different distances or speeds at different heights, letting you visually see which works best for your printer and filament combination.

### 2. Printing Temperature

The hotter the filament, the more liquid and prone to oozing it becomes.

!!! tip "Lower the Temperature"
    Try lowering the printing temperature in 5°C increments. Print with the lowest possible temperature (within the recommended range for the material) that still ensures good layer adhesion—this will significantly reduce stringing.

### 3. Filament Moisture

!!! danger "The Silent Enemy: Wet Filament"
    Hygroscopic filaments like **PETG, TPU, and Nylon** absorb moisture from the air. When the water in the filament is heated in the nozzle, it turns to steam and expands violently, pushing plastic out. This is a major cause of severe stringing. **Always dry your filament** if you suspect moisture.

### 4. Travel Speed

Increasing the speed of non-extrusion moves gives less time for filament to ooze. Increase the `Travel Speed` in your slicer to **150mm/s to 200mm/s** if your printer can handle it without skipping steps.

### Anti-Stringing Checklist
- [ ] Is the filament dry?
- [ ] Did you print a temperature tower to find the lowest viable temperature?
- [ ] Did you print a retraction tower to optimize distance and speed?
- [ ] Is travel speed set to a high value (≥150mm/s)?
- [ ] (Advanced) Did you enable the `Avoid Printed Parts When Traveling` option in your slicer?
