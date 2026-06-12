# Bridging Issues

!!! abstract "The Problem"
    **Bridging** is the printer's ability to print over an empty space between two points, creating a horizontal "bridge." The problem occurs when the bridge's lines sag, look messy, or fail to connect properly, instead of forming a straight, smooth surface.

<figure markdown="1">
  ![A comparison showing poor bridging next to a clean bridge](../../images/image-placeholder.png#only-light){ width="600" }
  ![A comparison showing poor bridging next to a clean bridge](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A comparison showing a poor bridge with sagging, drooping strands of filament next to a clean, straight bridge.</figcaption>
</figure>

## Common Causes and How to Fix Them

Successful bridging depends on a single factor: **cooling the extruded filament as fast as possible** so it solidifies in a straight line before gravity can pull it down.

### 1. Insufficient Cooling

This is the primary cause. If there isn't a strong, directed airflow over the filament line being printed, it will remain soft and sag.

* **Fix 1 (Slicer):** Go to your slicer's cooling settings and look for "Bridging Fan Speed" (or similar). Set this value to **100%**. This forces the fan to max speed only when it's bridging.
* **Fix 2 (Hardware):** Your printer's stock cooling duct may be inefficient. Consider printing an upgraded fan duct, like a "Satsana" or other popular design for your printer model. This directs air more effectively under the nozzle.

### 2. Printing Temperature Too High

Printing hotter makes the plastic more liquid, requiring more time to solidify.

* **Solution:** Print at the lowest possible temperature for your filament. Use a **Temperature Tower** to find the sweet spot. Lower temperatures result in significantly better bridges.

### 3. Incorrect Printing Speed

The speed of a bridge is a delicate balance.

* **Too Slow:** Gives gravity more time to make the filament sag.
* **Too Fast:** The filament doesn't have time to "stick" to the arrival point and can be dragged.

* **Solution:** Most slicers have a specific `Bridge Speed` setting. Experiment with moderate values, perhaps a bit slower than your normal print speed (e.g., 30-50 mm/s). The goal is for the filament to be stretched quickly between the two points and cooled instantly.

### 4. Part Orientation

The direction in which the bridge is printed can make a difference.

* **Solution:** If your part has a long bridge in one direction and a short one in another, try rotating the part 45 degrees on the build plate. This may force the slicer to print the bridge lines diagonally, making them shorter and easier to execute.

## Quick Checklist
- [ ] Set "Bridging Fan Speed" to 100% in the slicer.
- [ ] Lower the printing temperature to the minimum viable.
- [ ] Adjust the `Bridge Speed` in the slicer to a moderate value.
- [ ] Consider printing an improved cooling fan duct.
- [ ] (Advanced) Check the `Bridge Flow Ratio` setting; sometimes a value slightly over 100% (e.g., 105%) can help.