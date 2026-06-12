# Stringing or Oozing

"Stringing" (or "oozing") is the defect where small, fine strands of plastic are left behind on a printed model, especially between different parts of the model, creating a spider-web-like appearance.

!!! info "What Causes Stringing?"
    This problem occurs when molten plastic leaks from the nozzle as it moves from one point to another during a non-extruding "travel move." It is especially common with materials like PETG.

---
### Causes and Solutions

1.  **Incorrect Retraction Settings**
    * !!! success "Primary Solution"
        Retraction is the function that pulls the filament slightly back before a travel move to relieve pressure in the nozzle.
    * **Slicer Solution:** Increase the **Retraction Distance** in small increments (e.g., 0.5 mm at a time). You can also increase the **Retraction Speed**. Most filament profiles come with good baseline values, but wet or lower-quality filaments may require adjustments.

2.  **Printing Temperature Too High**
    * **Cause:** The higher the temperature, the more liquid the plastic becomes and the more likely it is to ooze from the nozzle.
    * **Solution:** Try lowering the printing temperature in 5°C increments. Print a "temperature tower" to find the sweet spot for your filament, where layer quality is good but stringing is minimal.

3.  **Wet Filament**
    * **Cause:** Materials like PETG, Nylon, and TPU absorb moisture from the air. The water in the filament turns to steam in the hot nozzle, pushing plastic out and causing both stringing and popping sounds.
    * **Solution:** Dry your filament in a filament dryer or a low-temperature oven before use. Store your spools in sealed bags with desiccant.

<figure markdown="1">
  ![Stringing Example](../images/image-placeholder.png#only-light){ width="600" }
  ![Stringing Example](../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with fine plastic strings between separate parts.</figcaption>
</figure>

!!! tip "Removing Light Stringing"
    If your finished part has only a few thin strings, you can easily remove them by quickly passing the flame from a lighter or a blast from a heat gun over the surface. The heat will cause the strings to shrink and disappear.