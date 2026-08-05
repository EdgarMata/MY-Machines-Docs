# Design Guide: Creating Dashed and Dotted Lines

Creating dashed or dotted lines is a useful technique for designing fold lines, perforated edges, or decorative borders. In **Neon Studio**, you can easily transform any continuous vector path into a dashed line using Path Effects.

---

## Step-by-Step: Applying the Dashed Stroke Effect

Follow these steps to convert a standard object (like a rectangle or a line) into a dashed path:

1.  **Select your Object:** Click on the object you wish to modify in the **Neon Studio** workspace.
2.  **Access Path Effects:** Navigate to the top menu and select **Path > Path Effects**.
3.  **Add a New Effect:** A panel will open on the right side of the screen. Click the **plus (+) button** to add a new effect.
4.  **Select Dashed Stroke:** In the effects selector window, scroll down until you find **Dashed Stroke** (Traço Tracejado) and select it.

---

## Customizing your Dashed Line

Once the effect is added, you can fine-tune the appearance of the dashes using the following parameters in the sidebar:

* **Number of Dashes:** This defines how many individual segments will make up the line. Increasing this number makes the dashes smaller and more frequent.
* **Hole Factor:** This controls the spacing (the "gap") between each dash. A higher factor creates a larger distance between segments.
* **Use Segments:** When enabled, the software calculates the number of dashes per individual segment of the path (e.g., each side of a square) rather than treating the entire object as a single continuous line. This helps maintain symmetry in geometric shapes.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Adjusting dashed stroke parameters in the Path Effects panel (Coming Soon)</figcaption>
</figure>

---

!!! success "Pro Tip for Folding"
    If you are creating a "fold line" on cardboard or paper, use a dashed line with a high **Hole Factor**. This tells the **Neon** to cut small slots, making the material easy to bend without snapping or cutting it completely through.

---
**Need help with specific fold settings?**
If you are designing complex packaging, contact **Neon Laser Support** for advice on the best dash-to-gap ratios for different material thicknesses.