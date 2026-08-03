# Under-extrusion

Under-extrusion is the opposite of over-extrusion: the printer is not pushing out enough plastic. This results in brittle prints with gaps, missing layers, or a spongy texture.

### Common Symptoms

* There are visible gaps between the lines of each layer.
* Layers do not bond well to each other, and the part breaks easily.
* Entire layers are missing in certain parts of the print.
* The print looks fragile, rough, or stringy.

### Causes and Solutions

1.  **Clogged Nozzle**
    !!! warning "Most Common Cause"
        A partially or fully clogged nozzle is the number one cause of under-extrusion.
        * **Solution:** Follow the **"Cleaning the Nozzle"** guide. Use the cleaning needle to clear the obstruction. If the problem persists, you may need to perform a "Cold Pull" or replace the nozzle.

    <figure markdown="1">
      ![Cold Pull Result](/assets/images/image-placeholder.webp#only-light){ width="610" }
      ![Cold Pull Result](/assets/images/image-placeholder.webp#only-dark){ width="610" }
      <figcaption>Illustration showing the result of a "Cold Pull": the tip of the removed filament has the exact shape of the nozzle's interior, pulling debris out with it.</figcaption>
    </figure>

2.  **Dirty Extruder Drive Gear**
    * **Cause:** Plastic debris can build up in the teeth of the gear that pushes the filament, causing it to slip.
    * **Solution:** Follow the **"Cleaning the Extruder (Drive Gear)"** guide and use a brush to clean the gear's teeth.

3.  **Calibrate the Flow Rate**
    * **Cause:** The flow rate value may be set too low.
    * **Solution:** In the printer's menu, go to `Tune -> Flow` and increase the value (e.g., from 95% to 100%). For a permanent fix, adjust it in your slicing software.

4.  **Printing Temperature Too Low**
    * **Cause:** If the nozzle temperature is too low for the material, the plastic becomes too viscous and difficult to extrude.
    * **Solution:** Increase the printing temperature in 5°C increments.

5.  **Under-extrusion on the First Layer**
    * **Cause:** If the problem only occurs on the first layer, the cause is a nozzle that is too far from the bed.
    * **Solution:** Adjust your "Live Adjust Z" to a more negative value.

<figure markdown="1">
  ![Under-Extrusion Example](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Under-Extrusion Example](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>Illustration of a print with gaps and missing layers due to under-extrusion.</figcaption>
</figure>
