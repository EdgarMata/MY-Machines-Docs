# Skipped or Missing Layers

!!! abstract "The Problem"
    **Skipped layers** (or missing layers) manifest as a clean, horizontal gap in the print. The printer seems to have stopped printing for one or more layers and then resumed, often causing the print to break into two or more separate pieces.

<figure markdown="1">
  ![A print that has split due to a missing layer](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![A print that has split due to a missing layer](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>A 3D print that has cleanly separated into two pieces due to one or more missing layers, indicating a temporary but complete failure of extrusion or Z-axis movement.</figcaption>
</figure>

## Common Causes and How to Fix Them

This issue indicates a temporary, total failure of either the extrusion system or the Z-axis movement system.

### 1. Temporary Extrusion Failure (Most Common)

The most likely cause is that the extruder stopped feeding filament for a short period and then recovered.

* **Cause: Filament Snag.** The filament spool may have gotten tangled or could not rotate freely, preventing the extruder from pulling more material.
    * **Solution:** Ensure your filament spool is mounted on a low-friction holder and can unwind without any hitches. Check the filament path from the spool to the extruder for any sharp bends or snags.
* **Cause: Temporary Clog.** A small piece of debris may have caused a temporary clog that eventually cleared itself.
    * **Solution:** While difficult to diagnose after the fact, if this happens repeatedly, it may be a sign of poor quality filament or [Heat Creep](../extrusion-issues/extrusion-problems.md).
* **Cause: Extruder Gear Skips.** The extruder gear may have briefly lost its grip on the filament (e.g., due to incorrect tension) and then regained it.
    * **Solution:** Check your extruder gear for built-up plastic dust and ensure the tension arm is applying firm, consistent pressure.

### 2. Z-Axis Binding or Sticking

This is a mechanical issue where the Z-axis fails to move up for one or more layers. The printer doesn't know this and continues trying to print at the same height. This usually creates a blobby, over-extruded mess for a few layers before the Z-axis breaks free and starts moving up again. In the final print, this messy section is very weak and breaks away, looking like a clean gap.

* **Solution:**
    * **Clean and Lubricate:** Thoroughly clean the Z-axis lead screw(s) and apply a fresh, thin coat of appropriate lubricant (e.g., white lithium grease).
    * **Check for Binding:** With the motors off, manually turn the Z-axis lead screw by hand. It should move smoothly throughout its entire range of travel. If you feel any tight spots, investigate for misalignment or overtightened wheels. Refer to the [Z-Axis Issues](./z-axis-issues.md) guide for more detail.

## Quick Checklist
- [ ] Check that your filament spool can rotate freely and is not tangled.
- [ ] Inspect the entire filament path for any points where it could snag.
- [ ] Clean and lubricate your Z-axis lead screw(s).
- [ ] Manually check the Z-axis for any binding spots.

