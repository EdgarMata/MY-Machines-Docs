# Pillowing

"Pillowing" is a defect that occurs on the top-most solid layer of a print. The surface fails to close properly, appearing bumpy and uneven, as if small "pillows" were forming over the infill.

!!! info "What Causes Pillowing?"
    This issue is almost always caused by **insufficient cooling** of the plastic and/or an **insufficient number of top solid layers**. The hot plastic sags into the gaps of the infill pattern below before it has a chance to solidify.

---
### Solutions (in the Slicer)

The solutions for pillowing are almost all configured in your slicing software.

1.  **Increase the Number of Top Solid Layers**
    * **Solution:** This is the most effective fix. If you are using 3 or 4 top layers, increase the value to 5 or 6. This provides more material and time for the surface to level out and solidify correctly.

2.  **Check the Part Cooling Fan**
    * **Cause:** If the fan blowing air onto the part is not running at 100% during the top layers, the plastic will not cool quickly enough.
    * **Solution:** Verify in your slicer that the fan speed is set to 100%. Also, physically check that the fan is clean and functioning correctly.

3.  **Decrease the Top Layer Print Speed**
    * **Solution:** Printing the top layers more slowly gives the fan more time to cool the plastic, helping to create a smoother surface.

<figure markdown="1">
  ![Pillowing Example](../images/image-placeholder.png#only-light){ width="600" }
  ![Pillowing Example](../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with a bumpy, uneven top surface.</figcaption>
</figure>