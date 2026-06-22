# Warping

Warping occurs when the corners of a print begin to lift and detach from the print bed during the printing process. This problem is more common with large parts and with materials that have high thermal shrinkage, such as ABS.

### Main Cause: Thermal Contraction

Warping happens because as the plastic cools, it shrinks. The upper layers cool faster than the lower layers (which are in contact with the hot bed), creating tension that pulls the corners of the part upwards.

### Solutions

1.  **Use a Brim or Skirt**
    !!! success "The Most Effective Solution"
        Enabling the **"Brim"** option in your slicing software is the most effective way to combat warping. The Brim creates a series of lines around the base of your part, increasing the surface area that adheres to the bed and helping to hold the corners down. A thicker "Skirt" printed close to the part can also help by creating a warmer microclimate around it.

    <figure markdown="1">
      ![Warping Example](/images/image-placeholder.png#only-light){ width="600" }
      ![Warping Example](/images/image-placeholder.png#only-dark){ width="600" }
      <figcaption>Illustration of a print with corners lifting off the print bed.</figcaption>
    </figure>

2.  **Ensure a Perfect First Layer**
    If the first layer adhesion is weak, warping is inevitable. Follow all the tips from the "Adhesion Issues" guide (clean bed, correct Z-height).

3.  **Use an Enclosure**
    For materials like ABS or ASA, printing inside an enclosure keeps the ambient temperature around the part higher and more stable. This reduces thermal shock and drastically decreases warping.

4.  **Adjust Temperatures and Cooling**
    * **Part Cooling Fan:** Turn off the part cooling fan for the first few layers. You can configure this in your slicing software.
    * **Bed Temperature:** Increasing the heatbed temperature can help keep the base of the part "stickier."
