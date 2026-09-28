# Your First Slice: A Basic Workflow

Once OrcaSlicer is configured with a **validated My-Cloner Rev A profile**, slicing a model follows a simple, repeatable workflow.

!!! warning "Rev A Profile Status"
    The final public Rev A profile package is not yet available. Do not use an unvalidated legacy profile for machine operation.

<figure markdown="1">
  ![Orca Slicer Interface](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Orca Slicer Interface](/assets/images/image-placeholder.webp#only-dark){ width="610" }
</figure>

---
## The Slicing Workflow

### Add a Model

First, get your 3D model file (`.stl`, `.step`, `.3mf`, etc.). You can either drag and drop the file directly onto the "Plater" (the virtual print bed) or use the "Add" icon in the top toolbar. You can also use the model manipulation tools (move, rotate, scale) on the left to position your model as needed.

### Select Your Printer Profile

On the left-hand settings sidebar, ensure that the **"My-Cloner Rev A"** is selected in the "Printer" dropdown menu. This loads all the machine-specific settings.

### Select Your Filament Profile

In the "Filament" dropdown, choose the material you have loaded into your printer (e.g., "Generic PLA"). This will apply the correct temperature, cooling, and retraction settings for that material.

### Select Your Print Quality Profile

In the "Process" dropdown, choose your desired quality and speed. These profiles are usually named by their layer height.
* `0.20mm Standard` is a great all-around choice for quality and speed.
* `0.28mm Draft` is faster but with more visible layer lines.
* `0.12mm Detail` is slower but produces a much finer surface finish.

### Slice and Preview!

1.  Click the **"Slice"** button in the top right. Orca Slicer will calculate all the toolpaths.
2.  After slicing, the view will switch to the **"Preview"** tab. This is a critical step!
3.  Use the vertical slider on the right to scrub through the layers of your print. Check the infill, supports, and walls to ensure everything looks as you expect.
4.  Once you are satisfied, you can use the **"Upload and Print"** button (if you have Klipper connected) or "Export G-code" to save the file.
