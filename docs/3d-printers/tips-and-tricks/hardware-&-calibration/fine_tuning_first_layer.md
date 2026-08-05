# Fine-Tuning the First Layer with Bed Mesh Correction 

Even after a successful automatic bed leveling (ABL), you might notice that your first layer is ever-so-slightly more "squished" on one side of the bed than the other. For perfectionists, Klipper offers a powerful tool to make micro-adjustments to the generated bed mesh.

!!! info "What is Bed Mesh Correction?"
    Your printer's ABL system probes a grid of points on the bed and creates a digital "mesh" to compensate for any warping. The `BED_MESH_CALIBRATE` command in Klipper allows you to manually adjust the height of each point in this mesh for ultimate control.

---
### How to Use Klipper's Bed Mesh Tuner

1.  **Generate a Bed Mesh:** First, ensure you have a saved bed mesh. Run `BED_MESH_CALIBRATE` followed by `SAVE_CONFIG` if you don't have one.
2.  **Start the Calibration Tool:** In the console, run the command `BED_MESH_CALIBRATE`.
3.  **Start a First Layer Test Print:** While the calibration tool is active, start printing a large, single-layer object (like a 200x200mm square).
4.  **Live-Tune the Mesh:**
    * As the nozzle moves across the bed, you will see its position reflected in the bed mesh map in your web interface.
    * If you notice an area is too high (not enough squish), you can use the `TESTZ Z=-` command to lower the nozzle in that specific area (e.g., `TESTZ Z=-0.02`).
    * If an area is too low (too squished), use `TESTZ Z=+` to raise it.
5.  **Accept and Save:** Once you have tuned the mesh to your liking across the entire bed, run the `ACCEPT` command. Finally, run `SAVE_CONFIG` to make the changes permanent.

<figure markdown="1">
  ![Klipper Bed Mesh Visualizer](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Klipper Bed Mesh Visualizer](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>An image of the Klipper bed mesh visualizer in Mainsail or Fluidd, showing the grid of probed points and their relative heights.</figcaption>
</figure>

!!! warning
    This is an advanced technique. For most users, a standard automatic bed level is sufficient. This is for chasing that "perfect" first layer.
