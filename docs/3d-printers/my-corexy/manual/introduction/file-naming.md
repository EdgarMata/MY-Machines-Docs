# File Naming Convention

To make organizing your prints easier, the project's STL files follow a specific naming convention. Understanding how to decipher it will help you know which color to use and how many copies of each part to print.

<figure markdown="1">
  ![Diagram of the file naming convention](../../images/image-placeholder.png#only-light){ width="600" }
  ![Diagram of the file naming convention](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A diagram illustrating a filename like "[a]z_belt_clip_lower_x4.stl" and pointing to each component: color prefix, part name, and quantity suffix.</figcaption>
</figure>

### Primary Color
Files that should be printed in your main color have no special prefix.
* **Example:** `z_joint_lower_x4.stl`

### Accent Color
Any part designated as an accent piece (to give your machine a pop of color) will have the `[a]` prefix at the beginning of the filename.
* **Example:** `[a]tensioner_left.stl`

### Quantity to Print
If a filename ends with the `_x#` suffix (where `#` is a number), that indicates the required number of copies you need to print of that part.
* **Example:** `[a]z_belt_clip_lower_x4.stl` - This means you need to print 4 copies of this part in your accent color.