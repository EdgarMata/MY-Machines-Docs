# Poor Layer Adhesion (Brittle Parts)

!!! abstract "The Problem"
    The print looks fine, but it breaks easily along the layer lines. The individual layers have not fused together correctly, resulting in an extremely weak part. This phenomenon is also called **delamination**.

<figure markdown="1">
  ![A 3D printed part breaking along its layer lines](/images/image-placeholder.png#only-light){ width="600" }
  ![A 3D printed part breaking along its layer lines](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A 3D printed part easily breaking along its layer lines, demonstrating poor layer adhesion or delamination.</figcaption>
</figure>

## Common Causes and How to Fix Them

Layer adhesion is a thermo-chemical reaction. The new hot layer must melt into the previous layer, which has already cooled slightly. If this fusion is incomplete, the bond will be weak.

### 1. Printing Temperature is Too Low

This is the number one cause. If the filament isn't hot enough, it won't have the energy to properly fuse with the layer below it.

* **Solution:** Increase the nozzle temperature in 5°C increments. Print a **Temperature Tower** to find the sweet spot for your filament, where strength is maximized without causing other issues like stringing.

### 2. Excessive Part Cooling

The part cooling fan may be blowing too hard, cooling the previous layer so quickly that the new hot layer cannot adhere.

* **Solution:** Reduce the part cooling fan speed in your slicer. For materials like PETG, a speed of 30-50% is common. For ABS/ASA, the fan should be off. For PLA, if you're having this issue, you can try reducing it to 70-80%.
* **Enclosures:** For materials like ABS/ASA, an enclosure is essential to keep the ambient temperature high and promote adhesion.

### 3. Under-Extrusion

If the printer is not depositing enough material, the layer lines will be too thin and won't have enough surface area to bond correctly.

* **Solution:** Calibrate your extruder's `E-steps` and the `Flow Rate` (or `Extrusion Multiplier`) in your slicer. Check for a partially clogged nozzle.

### 4. Printing Speed is Too High

Printing too fast may not give the filament enough time to fully melt in the hotend, resulting in a cooler extrusion and, consequently, poor adhesion.

* **Solution:** Reduce the overall print speed. If the problem persists, it could be a sign that your hotend cannot melt filament as fast as you are requesting (volumetric flow limit).

## Quick Checklist
- [ ] Increase printing temperature by 5-10°C.
- [ ] Print a Temperature Tower to find the ideal temperature.
- [ ] Reduce the part cooling fan speed.
- [ ] Check and calibrate extrusion (E-steps and Flow Rate).
- [ ] Reduce the print speed.