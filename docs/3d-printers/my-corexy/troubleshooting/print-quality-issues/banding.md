# Z-Axis Banding

!!! abstract "The Problem"
    **Z-Banding** manifests as a pattern of protruding or indented horizontal lines on the surface of the print. Unlike normal layer lines, these bands are inconsistent or have a visible repeating pattern.

<figure markdown="1">
  ![A close-up of a print's vertical surface showing Z-axis banding](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![A close-up of a print's vertical surface showing Z-axis banding](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>A close-up of a print's vertical surface showing a pattern of inconsistent, repeating horizontal lines, which is characteristic of Z-axis banding.</figcaption>
</figure>

## Common Causes and How to Fix Them

Z-Banding can be frustrating because the causes can be mechanical or extrusion-related.

### 1. Mechanical Issues in the Z-Axis

Any imperfection in your printer's vertical movement will be "printed" onto the walls of your part.

* **Dirty or Bent Lead Screw:**
    * **Solution:** Clean the Z-axis lead screw with a cloth and isopropyl alcohol to remove dust and old lubricant. Then, apply a thin layer of appropriate lubricant (like white lithium grease or Super Lube). To check if it's bent, remove it and roll it on a flat surface. If it wobbles, it's bent and should be replaced.
* **Loose or Misaligned Coupler:** The coupler that connects the Z-motor to the lead screw may be loose.
    * **Solution:** Ensure all grub screws on the coupler are tight.
* **Z-Wobble:** The lead screw may not be perfectly parallel to the frame, causing a wobbling motion as it rises.
    * **Solution:** Ensure the Z-motor mount and top bearing (if present) are not over-constraining the lead screw, allowing it a small amount of lateral movement to self-align.

### 2. Extrusion Inconsistency

If the amount of extruded plastic varies slightly from layer to layer, it will create thicker and thinner lines.

* **Unstable PID Tuning:** The nozzle temperature fluctuates during printing. Temperature variations change the plastic's viscosity, changing how it extrudes.
    * **Solution:** Perform a **"PID Tune" calibration** for your hotend. This process, done via a terminal like Pronterface or OctoPrint (command `M303 E0 S210 C8`), calibrates the heating algorithm to maintain a much more stable temperature.
* **Poor Quality Filament:** Variations in filament diameter along the spool cause inconsistent extrusion.
    * **Solution:** Measure the filament diameter at several points with calipers. If it varies more than +/- 0.05mm, the filament is low quality. Try using a more reputable brand.

### 3. Bed Temperature Issues

On some printers, the bed heater cycling on and off can cause minute expansion and contraction that reflects on the part.

* **Solution:** Perform a **"PID Tune" calibration** for your bed (command `M303 E-1 S60 C8`). This stabilizes the bed temperature, minimizing this effect.

## Quick Checklist
- [ ] Clean and lubricate the Z-axis lead screw(s).
- [ ] Check if the lead screw is bent.
- [ ] Perform a "PID Tune" for the hotend.
- [ ] Perform a "PID Tune" for the bed.
- [ ] Test with a high-quality roll of filament.
