# Bridging

"Bridging" is a 3D printer's ability to print a straight, horizontal line across an open gap, connecting two points of a model (creating a "bridge"). Good bridging results in a straight line with little to no sagging.

!!! info "How Does Bridging Work?"
    To create a bridge, the extruded plastic is stretched between the two points and cooled as quickly as possible so that it solidifies before it has time to droop.

---
### Problems and Solutions

* **Problem:** The bridge lines sag, look very messy and loose, or fail to connect the two points altogether.
* **Cause:** A combination of incorrect print speed and insufficient cooling.

### Solutions (in the Slicer)

Bridging settings are almost entirely controlled by your slicing software. Most good printing profiles already have optimized settings for bridging.

1.  **Maximize the Part Cooling Fan Speed (Bridge Fan Speed)**
    * **Solution:** This is the most important setting. Ensure that the fan speed for bridges is configured to **100%**.

2.  **Adjust the Bridge Print Speed**
    * **Solution:** This may seem counterintuitive, but effective bridging often requires a **relatively high print speed**. The high speed helps to stretch the filament quickly between the two points. However, if the speed is too high, the line might break. It's a matter of finding the right balance. Try printing a bridging test model and adjust the speed to see what works best for your material.

3.  **Lower the Printing Temperature**
    * **Solution:** Printing at the lowest possible temperature for your filament will cause it to solidify faster, resulting in cleaner bridges with less sagging.

<figure markdown="1">
  ![Bridging Example](../images/image-placeholder.png#only-light){ width="600" }
  ![Bridging Example](../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with successful bridging between two pillars.</figcaption>
</figure>
