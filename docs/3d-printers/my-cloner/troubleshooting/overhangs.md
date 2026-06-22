# Overhangs

Overhangs are parts of a model that are printed over empty space, without direct support from below. Your printer's ability to print quality overhangs depends heavily on the angle of the overhang and part cooling.

!!! info "The 45-Degree Rule"
    Most 3D printers can print overhangs up to an angle of **45 degrees** from the vertical without a significant loss in quality and without needing supports. Beyond this angle, the quality begins to degrade.

---
### Problems and Solutions

* **Problem:** The layers of the overhang curl upwards, droop, or have a very messy and rough appearance.
* **Cause:** The hot plastic is extruded partially into the air and, without rapid and effective cooling, it fails to solidify in the correct position, starting to sag or curl up due to the heat from the nozzle on the next pass.

### Solutions

1.  **Improve Part Cooling**
    * !!! success "Primary Solution"
        Strong, directed cooling is the key to good overhangs.
    * **Solution:** Make sure your **part cooling fan** is running at 100% speed (you can configure this in the slicer). Check that the fan and its air duct are clean and blowing directly at the area just below the nozzle.

2.  **Decrease Print Speed**
    * **Solution:** Printing the perimeters more slowly, especially on overhangs, gives the plastic more time to cool and solidify in the correct position. Look for settings like "Overhang Speed" in your slicer.

3.  **Use Supports**
    * **Solution:** For very steep overhangs (greater than 50-60 degrees) or for horizontal overhangs, the only reliable solution is to enable **supports** in your slicing software. The slicer will generate support structures that hold up the overhang and are removed after the print is finished.

<figure markdown="1">
  ![Overhangs Example](/images/image-placeholder.png#only-light){ width="600" }
  ![Overhangs Example](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with successful and failed overhangs.</figcaption>
</figure>