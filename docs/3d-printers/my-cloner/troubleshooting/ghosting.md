# Ghosting or Ringing

"Ghosting" (or "ringing") is a defect that appears as ripples or "ghosts" on the surface of a print, typically following sharp corners or distinct features.

!!! info "What Causes Ghosting?"
    This artifact is caused by **vibrations**. When the print head abruptly changes direction or stops, inertia causes the entire system to vibrate. These vibrations are transferred to the part and become visible on its surface.

---
### Causes and Solutions

1.  **Loose Belts**
    * **Cause:** Loose belts on the X or Y axes are the most common cause of ghosting. The slack in the belt allows vibration to propagate without being dampened.
    * **Solution:** Check and tighten your belts. They should be taut enough to produce a low-pitched sound when plucked, but not so tight that they restrict movement.

2.  **Unstable Printer Frame**
    * **Cause:** If the printer's frame is not rigid or if the printer is on a wobbly surface, any vibration will be amplified.
    * **Solution:** Ensure all frame screws are tight and that the printer is on a solid, stable surface.

3.  **Print Speeds and Acceleration Too High**
    * **Cause:** Higher speeds and accelerations generate more inertia and, consequently, more vibration.
    * **Slicer Solution:** Reduce the `Print Speed`, especially the `Outer Wall/Perimeter Speed`. For more advanced control, reducing the **Acceleration** and **Jerk** values in the slicer will have a significant impact on reducing ghosting.

<figure markdown="1">
  ![Ghosting Example](../images/image-placeholder.png#only-light){ width="600" }
  ![Ghosting Example](../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with faint, repeating patterns on its surface.</figcaption>
</figure>