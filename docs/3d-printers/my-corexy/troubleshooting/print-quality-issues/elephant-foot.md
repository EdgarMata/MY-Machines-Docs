# Elephant's Foot

!!! abstract "The Problem"
    **Elephant's Foot** is a printing defect where the base of the part is visibly wider than the layers above it, as if the model is being "squashed" against the print bed, creating a small lip or rim.

<figure markdown="1">
  ![The base of a 3D print showing Elephant's Foot](/images/image-placeholder.png#only-light){ width="600" }
  ![The base of a 3D print showing Elephant's Foot](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>The base of a 3D print showing the first few layers bulging outwards, wider than the rest of the model, which is known as Elephant's Foot.</figcaption>
</figure>

## Common Causes and How to Fix Them

This problem is almost always a combination of two things: the nozzle being too close to the bed and/or the bed being too hot.

### 1. Z-Offset is Too Low

This is the most likely cause. To ensure good first-layer adhesion, we often calibrate the nozzle to be very close to the bed. If it's too close, the first layer of filament gets squashed and forced outwards, creating the bulge.

* **Solution:** Slightly increase your `Z-Offset` (or level your bed with the nozzle a tiny bit higher). Do this in small increments of `+0.02mm` or `+0.05mm` until the elephant's foot disappears while still maintaining good first-layer adhesion. It's a fine balance.

### 2. Bed Temperature is Too High

If the bed temperature is too high, the first few layers of the model remain in a semi-liquid state for longer. The weight of the rest of the print on top of these soft layers can cause them to bulge outwards.

* **Solution:** Lower your print bed temperature in 5°C increments. For PLA, if you're using 65°C or 70°C, try dropping to 60°C or 55°C.

### 3. First Layer Over-Extrusion

Some slicer profiles, by default, increase the material flow rate for the first layer to ensure good adhesion. If this value is excessive, it can contribute to elephant's foot.

* **Solution:** Check your slicer settings and ensure the `First Layer Flow` is not set to a very high value (e.g., >105%). Try resetting it to 100%.

### 4. A Fix at the Model (Design) Level

If you can't completely eliminate the problem with printer adjustments, or if you need very precise dimensions at the base, you can compensate in the design.

* **Solution:** Add a small **chamfer** to the base of your model. A `0.2mm` to `0.4mm` chamfer at 45 degrees is usually enough to compensate for the lateral expansion of the elephant's foot, resulting in a final part with a perfect 90-degree base.

## Quick Checklist
- [ ] Increase the Z-Offset in small increments.
- [ ] Lower the print bed temperature by 5°C.
- [ ] Check that the first layer flow is not excessively high in the slicer.
- [ ] (In Design) Add a small chamfer to the base of the part.