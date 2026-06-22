# Infill Issues

!!! abstract "The Problem"
    The infill of the part is weak, crumbly, has gaps, or does not connect properly to the perimeters (walls) of the print. While not visible from the outside, poor infill drastically compromises the part's strength.

<figure markdown="1">
  ![A print with sparse, broken, or disconnected infill](/images/image-placeholder.png#only-light){ width="600" }
  ![A print with sparse, broken, or disconnected infill](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>The internal infill structure of a print looking sparse, broken, or disconnected from the outer walls.</figcaption>
</figure>

## Common Causes and How to Fix Them

Infill problems are often a sign that you are trying to print that specific part of the model too fast for what your hotend can handle.

### 1. Infill Speed is Too High

In slicers, the infill speed is often set to a much higher value than the wall speed to save time. However, if it's too high, the hotend may not be able to melt the plastic in time, resulting in under-extrusion only on the infill.

* **Solution:** Lower the `Infill Speed` in your slicer. Try setting it to the same value as your `Outer Wall Speed` for a test. If the problem disappears, you can start increasing it gradually to find your printer's limit.

### 2. Incorrect Infill Pattern

Some infill patterns are more challenging than others. Patterns that cross over themselves in the same layer (like "Grid") can cause issues because the nozzle has to travel over an already printed line of plastic, which can lead to material buildup on the nozzle.

* **Solution:** Switch to an infill pattern that does not cross over itself on the same layer.
    * **Gyroid:** An excellent choice. It's strong in all directions, fast to print, and non-crossing.
    * **Lines** or **Zig-Zag:** Simple and fast patterns.

### 3. Insufficient Infill/Perimeters Overlap

This slicer setting controls how much the infill overlaps with the inner walls of the part. If this value is too low, there will be a gap between the infill and the walls, resulting in a hollow, weak part.

* **Solution:** Increase the `Infill/Perimeters Overlap` (or `Infill Overlap Percentage`) value. A value between **25% and 30%** is a good starting point to ensure a strong bond.

### 4. General Under-Extrusion

If the problem isn't just with the infill, but with the entire part, you may be suffering from general under-extrusion.

* **Solution:** Check for common causes of under-extrusion: a partially clogged nozzle, uncalibrated `E-steps`, or incorrect filament diameter in the slicer.

## Quick Checklist
- [ ] Lower the infill speed (`Infill Speed`).
- [ ] Change the infill pattern to `Gyroid` or `Lines`.
- [ ] Increase the `Infill Overlap` to 25-30%.
- [ ] Make sure you are not suffering from general under-extrusion.