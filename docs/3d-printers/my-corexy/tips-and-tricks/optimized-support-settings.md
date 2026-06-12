title: Guide to Optimizing Support Settings
description: Learn how to configure supports in your slicer to be effective, use less material, and most importantly, be easy to remove without damaging the part.
---

# Guide to Optimizing Support Settings

Nobody likes using supports. They increase print time, waste material, and leave marks on the part. However, for complex geometries with steep overhangs, they are a necessary evil. The goal is to make them as efficient and easy to remove as possible.

### Support Types: Normal vs. Tree

=== "Normal (Grid / Lines)"
    Normal supports create a scaffold pattern (grid or lines) that rises directly from the bed to the area that needs support.
    * **Pros:** Very stable and predictable. Ideal for supporting flat, large surfaces.
    * **Cons:** Use more material and are harder to remove. The contact with the part is extensive, leaving more marks.

=== "Tree"
    Tree supports (popularized by Cura and now available in PrusaSlicer and others) grow like branches from the base, curving around the part to touch only the essential points.
    * **Pros:** Use significantly less material. Much easier to remove. The contact point with the part is minimal, leaving fewer marks.
    * **Cons:** May be less stable for very large or heavy areas. Slicer calculation can be slower.

!!! tip "When to choose Tree Supports?"
    For organic figures, miniatures, or any part with overhangs in hard-to-reach places, tree supports are almost always the best choice.

### Key Settings for Easy Removal

The "magic" for easy-to-remove supports is in the "gaps" left between the support and the part.

1.  **Support Z Distance:** **This is the most important setting.** It's the vertical gap between the top of the support and the bottom of the model.
    * A good starting point is **1 to 2 times your layer height**. If you print with 0.2mm, try a Z distance of `0.2mm` to `0.4mm`. A larger gap makes the support easier to remove, but the surface above it will have a rougher finish.

2.  **Support XY Distance:** The horizontal gap between the support and the vertical wall of your part. A value between **`0.7mm` and `1.0mm`** usually works well, preventing the support from fusing to the part.

3.  **Support Density:** You don't need solid supports. A density of **10% to 20%** with a pattern like "zig-zag" or "lines" is more than enough, saves material, and makes supports easier to crush and remove.

4.  **Support Interface:** This option creates a dense "roof" and/or "floor" in the support, exactly where it touches the part.
    * **Pro:** Creates a smoother surface for the first layer of your part to sit on, drastically improving the finish of the overhang.
    * **Con:** Makes the support a bit harder to remove, as the contact area is larger. It's a worthwhile trade-off for visible parts.