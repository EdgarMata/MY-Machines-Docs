# Layer Adhesion Issues

One of the most common problems in 3D printing is the first layer not adhering correctly to the print bed. If the first layer isn't perfect, the entire print is destined to fail.

### Main Cause: Incorrect "Live Adjust Z" Calibration

In most cases, lack of adhesion is due to the nozzle being too far from the print bed on the first layer.

* **Symptom:** The extruded plastic lines look round and do not connect to each other. The part easily detaches from the bed.
* **Solution:** You need to decrease the distance between the nozzle and the bed. While the first layer is printing, go to the `Tune` menu and adjust the **"Live Adjust Z"** value to a more negative number (e.g., from -0.600 to -0.650). Continue adjusting until the plastic line is slightly "squished" onto the bed, with a flat appearance and well-bonded to the adjacent lines.

<figure markdown="1">
  ![Layer Adhesion Example](../images/image-placeholder.png#only-light){ width="600" }
  ![Layer Adhesion Example](../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with layers that are not properly bonded together.</figcaption>
</figure>

### Secondary Cause: Dirty Print Surface

Grease from fingerprints, dust, or residue from previous prints can prevent good adhesion.

!!! tip "Keep Your Bed Clean"
    * **Regular Cleaning:** Before printing, wipe the bed with a paper towel and Isopropyl Alcohol (IPA) with a concentration of 90% or higher.
    * **Deep Cleaning:** If adhesion continues to be a problem, wash the bed with warm water and a few drops of dish soap to remove all grease.

### Other Solutions

* **Use a Brim in the Slicer:** For parts with a small contact area on the bed, enabling the "Brim" option in your slicing software (like PrusaSlicer) creates a flange around the part, increasing the surface area and improving adhesion.
* **Increase Temperatures:** Increasing the heatbed temperature by 5-10°C can help the plastic adhere better.
* **Adhesion Aids:** For difficult materials like Nylon or ABS, applying a thin layer of a glue stick (PVA) may be necessary to ensure adhesion.