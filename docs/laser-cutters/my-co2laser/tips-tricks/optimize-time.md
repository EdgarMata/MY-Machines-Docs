# Optimizing Production Time: Efficient Cutting and Engraving

Time is your most valuable resource. In this guide, we will show you how to organize your files in **Neon Studio** to minimize "travel time" and maximize the productivity of your **Neon**.

---

## Understanding how Neon Studio Processes Tasks

The **Neon Studio** always follows a top-to-bottom priority based on your **Layers**. This means the machine will always complete everything in the top layer before moving to the one below it.

### The Problem: Random Paths within a Layer
If you have a single layer containing many small, disconnected elements (like 50 circles), the software might process them in a non-linear order. Instead of going from circle 1 to circle 2, the laser head might jump from circle 1 to circle 30, then back to 5. These long "empty" movements add up and waste time.

---

## Strategy 1: The Multi-Layer Method

For maximum efficiency, you can force the **Neon** to follow a specific sequence by separating elements into multiple layers.

1.  **Sequence your items:** Decide the logical path for the laser (e.g., left to right, top to bottom).
2.  **Assign Layers:** Move the first group of items to Layer 1, the second to Layer 2, and so on.
3.  **Result:** The machine will strictly follow your numerical order, eliminating unnecessary diagonal travel across the workbed.

<figure markdown="span">
  ![](../images/construcao-light.png#only-light){ width="400" }
  ![](../images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Using numbered layers to dictate a precise laser path (Coming Soon)</figcaption>
</figure>

---

## Strategy 2: Grouping by Proximity

If creating a layer for every single item is too time-consuming, the **Grouping** strategy is a great middle-ground.

1.  **Identify Zones:** Divide your project into logical zones (e.g., a "Left Zone," "Center Zone," and "Right Zone").
2.  **Group and Layer:** Group the items within each zone and move each group to its own layer.
3.  **Result:** The **Neon** will finish all tasks in the first zone before traveling to the next, significantly reducing the total distance covered by the laser head.

---

## Summary Checklist for Faster Production:

* **Prioritize Engraving:** Always place engraving layers at the top so they are finished before the material is cut and potentially shifts.
* **Logic over Chaos:** Even a simple 3-layer split (Left, Middle, Right) can save minutes on a large-scale project.
* **Check the Preview:** Use the "Preview" function to visualize the laser's path before hitting "Neon It!".

---

!!! success "Pro Tip"
    When engraving text across a wide area, it is often faster to engrave each word individually (using layers) rather than having the laser head travel across the entire width of the machine for every single line of pixels.

---
**Want to shave more seconds off your timer?**
If you have a specific complex file, send it to **Neon Laser Support**. Our team can help you optimize the vector paths for peak performance.