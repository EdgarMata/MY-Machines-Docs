# Elephant Foot

"Elephant Foot" is a printing defect where the first few layers of the part are wider than the rest, creating a small lip or "squish" at the base.

## Main Cause: Nozzle Too Close to the Bed

This problem is almost always caused by a single thing: the extruder nozzle is too close to the print bed on the first layer.

* **What Happens:** When the nozzle is too low, it squeezes the plastic outwards because there isn't enough vertical space for the amount of plastic being extruded. This effect is usually confined to the first 1-3 layers.

## Solution

The solution is simple and direct: increase the distance between the nozzle and the bed.

* **Recheck the Z offset:** If the nozzle is too close to the print surface, recalibrate the P.I.N.D.A. Z offset using the validated Klipper procedure. Make small changes and verify the first layer after each adjustment.
* **Objective:** The goal is to find the point where the first layer adheres perfectly without being excessively squashed.

<figure markdown="1">
  ![Elephant Foot Example](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Elephant Foot Example](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>Illustration of a print with a widened first layer, resembling an elephant's foot.</figcaption>
</figure>

!!! tip "Small Adjustments Make a Big Difference"
    When fine-tuning the Z offset, use small controlled increments and verify the result carefully. Save only a value that has been confirmed on the physical machine.

