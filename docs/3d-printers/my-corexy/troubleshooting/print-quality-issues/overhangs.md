# Overhang Issues

!!! abstract "The Problem"
    An **overhang** is any part of the print that is printed at an angle to the vertical, without direct support underneath. The problem occurs when these sections have a very poor finish, with drooping lines, upward curling, or improper adhesion.

<figure markdown="1">
  ![A close-up of a messy overhang on a 3D print](../../images/image-placeholder.png#only-light){ width="600" }
  ![A close-up of a messy overhang on a 3D print](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A close-up of an angled overhang on a 3D print showing drooping loops and a rough, messy surface finish due to poor cooling.</figcaption>
</figure>

## Common Causes and How to Fix Them

Like bridging, good overhang performance depends almost exclusively on **cooling the filament as quickly as possible** so it solidifies before it has time to droop or deform. Most stock printers can handle angles up to 45-50 degrees without issue. Above that, quality begins to degrade.

### 1. Insufficient Cooling

This is the main cause. If the airflow from your part cooling fan is not powerful or well-directed, the plastic will remain soft for too long.

* **Fix 1 (Slicer):** Ensure your `Fan Speed` is at 100% for materials like PLA. Check if your slicer has an option to `Increase fan speed for overhangs`.
* **Fix 2 (Hardware):** The most significant improvement comes from installing a more efficient cooling duct (`fan duct`). Designs that offer dual-sided or 360° cooling (like the Satsana) make a huge difference.

### 2. Printing Temperature Too High

Printing hotter makes the plastic more liquid, making it more susceptible to drooping under gravity.

* **Solution:** Lower the printing temperature. Use the lowest temperature in the recommended range for your filament that still gives you good layer adhesion. A **Temperature Tower** is the ideal tool to find this point.

### 3. Printing Speed Too High

Printing overhangs quickly doesn't give the cooling fan enough time to act.

* **Solution:** Most slicers have specific speed settings for overhangs. Enable this feature and configure it to drastically reduce speed based on the overhang angle. For example:
    * 25% incline -> 80% speed
    * 50% incline -> 60% speed
    * 75% incline -> 40% speed

### 4. Layer Height Too Large

Larger layer heights (e.g., 0.28mm or 0.32mm) create more difficult overhangs because the overlap between one layer and the next is smaller.

* **Solution:** If overhang quality is critical, use a smaller layer height (e.g., 0.12mm or 0.16mm). Thinner layers get more support from the previous layer, allowing for steeper angles.

## Quick Checklist
- [ ] Increase the part cooling fan speed to 100%.
- [ ] Print and install an improved cooling fan duct.
- [ ] Lower the printing temperature by 5-10°C.
- [ ] Enable and configure overhang-specific print speeds in the slicer.
- [ ] Use a lower layer height for critical overhangs.
- [ ] If the angle is greater than 60-70 degrees, consider using supports.