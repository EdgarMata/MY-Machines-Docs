# Infill Issues

The infill is the internal support structure of your print. Problems with the infill can lead to weak parts or failures in the top solid layers.

!!! info "Infill Problems are Symptoms"
    Typically, weak, stringy, or gappy infill is not a problem with the infill setting itself, but rather a symptom of another printing issue, such as under-extrusion.

---
### Causes and Solutions

1.  **Weak or Incomplete Infill (with Gaps)**
    * **Main Cause:** Under-extrusion. Since infill is often printed much faster than the walls, extrusion problems will manifest there first.
    * **Solution:** Follow the **Under-extrusion Troubleshooting Guide**. The most likely culprits are a clogged nozzle or a printing temperature that is too low for the speed at which the infill is being printed.

2.  **Infill Speed Too High**
    * **Cause:** Most printing profiles are configured to print infill at a much higher speed than the walls to save time. However, if the speed is excessive, the hotend may not be able to melt the plastic fast enough, resulting in weak infill.
    * **Slicer Solution:** Reduce the **Infill Speed** to a value closer to the wall speed.

3.  **Infill Percentage Too Low**
    * **Cause:** If you are using a very low infill percentage (e.g., 5-10%), there may not be enough support for the top solid layers, causing them to droop, collapse, or show "pillowing."
    * **Solution:** For functional parts, use an infill of at least 15-20%. If you need a perfect top surface, a higher infill percentage can help.

<figure markdown="1">
  ![Infill Issues Example](/images/image-placeholder.png#only-light){ width="600" }
  ![Infill Issues Example](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with weak or poorly formed infill.</figcaption>
</figure>
