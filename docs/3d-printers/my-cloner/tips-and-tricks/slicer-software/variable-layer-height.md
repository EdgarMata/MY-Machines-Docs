# Using Variable Layer Height for Faster, Detailed Prints

Do you have a model that needs fine details on some parts but has large, simple vertical sections on others? Using the "Variable Layer Height" feature in your slicer is a powerful trick to optimize both print time and quality.

!!! info "What is Variable Layer Height?"
    Instead of printing the entire model with a single, fixed layer height (e.g., 0.2mm), this tool allows you to have different layer heights in the same print. You can use thin layers (e.g., 0.1mm) for detailed, curved surfaces and thick layers (e.g., 0.3mm) for straight, vertical sections.

---
### The Benefit: Best of Both Worlds

* **Quality Where It Matters:** You get high-resolution surfaces on the parts of the model that need it most.
* **Speed Where It Doesn't:** You save a significant amount of print time by using thicker, faster layers on simple sections.

### How to Use It (General Slicer Steps)

1.  **Slice the Model:** First, slice your model with a standard profile (e.g., 0.2mm).
2.  **Activate the Tool:** Find the "Variable Layer Height" tool in your slicer (in PrusaSlicer, it's an icon in the left-hand toolbar).
3.  **Adjust the Layers:** A new panel will appear next to your model in the preview. You can use your mouse to "paint" the areas of the model where you want finer detail or smoother surfaces. The slicer will automatically transition the layer heights.
4.  **Re-slice and Print:** Once you are happy with the adjustments, re-slice the model. The new G-code will contain all the instructions for changing the layer height automatically during the print.

<figure markdown="1">
  ![Variable Layer Height in Slicer](../../images/image-placeholder.png#only-light){ width="600" }
  ![Variable Layer Height in Slicer](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>An image of a model in a slicer's preview window, showing different color bands that represent varying layer heights along the Z-axis.</figcaption>
</figure>