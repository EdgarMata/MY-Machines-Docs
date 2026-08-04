# Stringing or Oozing (Hairy Prints)

!!! abstract "The Problem"
    **Stringing** (or oozing) is the occurrence of thin, web-like strands of plastic that form between different parts of a model as the print head moves over an open space.

<figure markdown="1">
--8<-- "image-placeholder.md"
  <figcaption>A 3D print covered in thin, web-like strands of plastic, a classic example of stringing or oozing.</figcaption>
</figure>

## Common Causes and How to Fix Them

Stringing is caused by molten filament leaking from the nozzle during moves where no extrusion should be happening. The solution is to minimize this oozing.

### 1. Incorrect Retraction Settings

Retraction is the function that pulls filament back into the hotend before a travel move. It's meant to relieve pressure in the nozzle to stop oozing. It is your main weapon against stringing.

* **Retraction Distance:** The length of filament (in mm) that is pulled back.
    * **Direct Drive:** Start with low values: `0.5mm` to `2.0mm`.
    * **Bowden:** Requires longer distances: `4.0mm` to `6.0mm`. Excessive distance can cause clogs.
* **Retraction Speed:** How fast the filament is pulled back. Start with a speed between `25mm/s` and `45mm/s`.

!!! success "Use a Retraction Tower"
    The most efficient way to find your ideal settings is to print a **retraction tower**, which tests different settings at various heights.

### 2. Printing Temperature Too High

The hotter the filament, the more liquid and "runny" it becomes, and the more easily it oozes.

* **Solution:** Lower the nozzle temperature in 5°C increments. Print at the lowest possible temperature that still ensures good layer adhesion.

### 3. Wet Filament

Hygroscopic filaments like PETG, TPU, and Nylon absorb moisture from the air. The water in the filament turns to steam in the hot nozzle and violently expands, pushing plastic out. This is a major cause of severe stringing.

* **Solution:** Dry your filament. Use a dedicated filament dryer or a food dehydrator at a low temperature (check recommendations for each material). Store filaments in sealed bags with desiccant.

### 4. Travel Speed

Faster travel moves give the filament less time to ooze.

* **Solution:** Increase the `Travel Speed` in your slicer. Values of `150mm/s` or more are common and effective, as long as your printer can handle it without skipping steps.

## Quick Checklist
- [ ] Print a retraction tower to find the ideal distance and speed.
- [ ] Print a temperature tower and use the lowest viable temperature.
- [ ] Dry your filament, especially if it is PETG, TPU, or Nylon.
- [ ] Increase Travel Speed to >150mm/s.
- [ ] (Advanced) Enable `Wipe` and `Coasting` settings in your slicer.
