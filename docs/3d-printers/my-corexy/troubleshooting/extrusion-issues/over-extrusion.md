# Over-Extrusion

!!! abstract "The Problem"
    **Over-extrusion** is the opposite of under-extrusion: the printer is pushing out more material than is necessary. This results in prints with poor dimensional accuracy, blobby surfaces, loss of fine detail, and stringing.

<figure markdown="1">
  ![A print showing signs of over-extrusion](../../images/image-placeholder.png#only-light){ width="600" }
  ![A print showing signs of over-extrusion](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A 3D print showing clear signs of over-extrusion, with blobby corners, messy top surfaces, and a loss of fine detail.</figcaption>
</figure>

## Common Causes and How to Fix Them

Fixing over-extrusion is usually more straightforward than fixing under-extrusion, as it's almost always a calibration issue.

### 1. Incorrect Flow Rate / Extrusion Multiplier

This is the cause in 99% of cases. The slicer is simply commanded to push out too much plastic, often because the setting is at its default of 100% (or 1.0) when the specific filament or printer needs less.

* **Solution: Calibrate Flow Rate.** This is the exact same process as for under-extrusion. Print a hollow cube with a single wall and no top layers. Use calipers to measure the wall thickness. If you requested a 0.4mm wall and it measures 0.45mm, you are over-extruding. Adjust the `Flow Rate` in your slicer downwards (e.g., from 100% to 90%) using the formula: `(Expected thickness / Actual thickness) * Current Flow Rate`.

### 2. Uncalibrated E-Steps

If your printer's firmware thinks it needs more motor steps to push 1mm of filament than it actually does, it will consistently push too much material.

* **Solution: Calibrate E-Steps.** While less common to be the primary cause than flow rate, it's a fundamental calibration. Follow a guide for "E-step calibration" to ensure your printer's baseline extrusion is accurate.

### 3. Printing Temperature Too High

While a minor factor, an excessively high printing temperature can lower the filament's viscosity, causing it to flow more freely from the nozzle. This can contribute to a slight over-extrusion effect and make problems like blobbing worse.

* **Solution:** Ensure you are not printing hotter than necessary. Print a **Temperature Tower** to find the optimal temperature for your filament, which provides good layer adhesion without being excessively hot.

## Quick Checklist
- [ ] **Calibrate your `Flow Rate` / `Extrusion Multiplier`. This is the most important step.**
- [ ] Perform an E-step calibration to ensure the printer's baseline is correct.
- [ ] Verify your print temperature is not excessively high for your filament.
- [ ] Ensure the filament diameter set in your slicer (e.g., 1.75mm) is correct.