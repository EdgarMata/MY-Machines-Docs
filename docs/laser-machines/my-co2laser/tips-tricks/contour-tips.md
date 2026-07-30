# Design Tips: Working with Contours and Outlines

To achieve a professional finish on your **Neon**, it is essential to prepare your design files correctly. This guide focuses on converting objects into paths and managing the execution order for perfect precision.

---

## I. Converting to Path (Object to Path)

For the **Neon Studio** to recognize the edges of your design as a vector line to follow, you must convert your objects into "Paths."

### The Process:
1.  Select your object in Inkscape.
2.  Navigate to the top menu: **Path > Object to Path**.
    * This tells the software that the shape is no longer a generic "square" or "text," but a specific coordinate-based path for the laser to follow.

!!! warning "Double Line Alert"
    If you apply "Stroke to Path" on a thick line, the laser will interpret it as two separate lines (one for each side of the stroke). This may result in a "burnt" or messy finish. For clean contours, ensure you are working with a single hairline vector.

---

## II. Generating G-Code for Contours

Once your design is converted to a path, you can generate the instructions for the **Neon**:

1.  Select the design.
2.  Go to **Extensions > Neon Studio > Contour**.
3.  If the "Neon" extension is missing, please ensure you have installed the **Neon Plug-ins** for Inkscape.

### Number of Passes:
Unlike heavy cutting, contouring (often used for marking or light outlines) usually requires only **one pass**. Increasing the passes on a contour job may overburn the material and reduce detail.

<figure markdown="span">
  ![](../images/construcao-light.png#only-light){ width="400" }
  ![](../images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Setting the number of passes in the Neon extension (Coming Soon)</figcaption>
</figure>

---

## III. Execution Order: Contour vs. Cut

The order in which the **Neon** executes tasks is vital for accuracy. When a piece is fully cut (detached from the main sheet), it may shift slightly due to gravity or air assist.

* **The Rule:** Always perform **Contours and Engravings first**, and the **Final Cut last**.
* **Reasoning:** If you cut the external shape first and then try to contour a detail inside it, the piece might have moved, causing the design to be off-center.

---

!!! success "Pro Tip"
    In **Neon Studio**, organize your project using layers. Place the "Contour" layer above the "Cut" layer to ensure the machine follows the correct priority automatically.

---
**Need help with your design files?**
If your contours are not appearing correctly in the preview, contact **Neon Laser Support** for a file optimization walkthrough.