# Understanding Key Print Settings

While the provided profiles are a great starting point, understanding what the key settings do will allow you to fine-tune your prints for perfect results. These settings are found in the "Process" tab on the left sidebar.

---
### First Layer Settings

!!! success "The Most Important Layer"
    A perfect print starts with a perfect first layer. These settings help you achieve strong bed adhesion.
* **First Layer Height:** Often slightly thicker than the other layers to ensure a good "squish" and strong adhesion.
* **First Layer Speed:** Printing the first layer much slower than the rest of the print gives the plastic time to bond securely to the print surface.
* **First Layer Temperatures:** You can set slightly higher nozzle and bed temperatures for the first layer to improve adhesion.

---
### Filament Profiles: The Core Settings

A filament profile contains all the settings specific to a material type.

* **Temperatures:** This section sets the nozzle and bed temperatures for the first layer and all other layers. This is the most important setting to adjust between different materials (e.g., PLA vs. PETG).
* **Cooling:** This controls the speed of your part cooling fan. Materials like PLA need 100% fan speed for quality, while materials like ABS/ASA need very little cooling to prevent cracking.
* **Retraction:** These settings tell the printer how much to pull the filament back to prevent stringing. Each material may require slightly different retraction settings.

---
### Print Speed vs. Quality

* **Layer Height:** This is the primary driver of quality and speed. A smaller layer height (e.g., 0.12mm) creates a much smoother, more detailed surface but takes significantly longer to print. A larger layer height (e.g., 0.28mm) is much faster but the layer lines will be more visible.
* **Speeds:** You can independently control the speed for different parts of the print. The most important are:
    * **Outer Wall / Perimeter:** Slower for a better surface finish.
    * **Infill:** Faster to save time, as it's not visible.
    * **Travel Moves:** Very fast, as no plastic is being extruded.

---
### Support Structures & Bed Adhesion

* **Supports:**
    * **When to use them?** Use supports when your model has "overhangs"—parts that would otherwise be printed in mid-air. A good rule of thumb is to enable supports for any overhang steeper than 45-50 degrees.
    * **Types:** "Normal" supports are straight columns, while "Tree" supports create organic, branch-like structures that are often easier to remove.

* **Bed Adhesion (`Skirt`, `Brim`, `Raft`)**
    * **Skirt:** A simple outline drawn around the part before the print starts. It's used to prime the nozzle and ensure a smooth flow of plastic. It does not touch the model.
    * **Brim:** A series of lines attached to the very first layer of your model. It's used to increase the surface area on the print bed, providing much stronger adhesion and preventing warping on large parts.
    * **Raft:** A thick grid of material that is printed first, on top of which your model is printed. It's used for very difficult-to-print materials or models with a tiny footprint, but it can be difficult to remove and affects the bottom surface finish.