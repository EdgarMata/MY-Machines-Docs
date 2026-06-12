# Elephant Foot

"Elephant Foot" is a printing defect where the first few layers of the part are wider than the rest, creating a small lip or "squish" at the base.

### Main Cause: Nozzle Too Close to the Bed

This problem is almost always caused by a single thing: the extruder nozzle is too close to the print bed on the first layer.

* **What Happens:** When the nozzle is too low, it squeezes the plastic outwards because there isn't enough vertical space for the amount of plastic being extruded. This effect is usually confined to the first 1-3 layers.

### Solution

The solution is simple and direct: increase the distance between the nozzle and the bed.

* **Adjust the "Live Adjust Z":** While the first layer is printing, go to the `Tune` menu and adjust the **"Live Adjust Z"** value to a **less negative** number (e.g., from -0.800 to -0.750). This slightly raises the nozzle.
* **Objective:** The goal is to find the point where the first layer adheres perfectly without being excessively squashed.

<figure markdown="1">
  ![Elephant Foot Example](../images/image-placeholder.png#only-light){ width="600" }
  ![Elephant Foot Example](../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with a widened first layer, resembling an elephant's foot.</figcaption>
</figure>

!!! tip "Small Adjustments Make a Big Difference"
    When adjusting the "Live Adjust Z," do it in small increments (0.02 to 0.05 mm) and observe the result in real-time.
