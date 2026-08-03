# Troubleshooting Design Discrepancies

If the final output on your material doesn't match what you see on your screen, it is usually due to software configuration or specific vector properties. This guide will help you identify and resolve the most common alignment and scaling issues.

---

## Geometric Distortions and Node Density

If a curved line appears jagged or straightens out unexpectedly, your vector likely has insufficient **nodes**. Nodes are the coordinate points that instruct the laser on its path. Low node density prevents the machine from executing smooth curves.

### How to optimize vector paths:
To ensure fluid movement and high fidelity to your original design, you can manually increase the node count within the editor.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Video: Optimizing Node Density for Smooth Curves (Coming Soon)</figcaption>
</figure>

---

## Dimensional Accuracy and Scaling Issues

When the physical size of the cut differs from your digital project, check the following factors:

### Import Errors and Workspace Conflicts
Scaling issues often occur during the file import process. If the dimensions are incorrect, try copying the design into a fresh workspace. 
* **Important:** Ensure only one instance of **Due Studio** is active to avoid communication conflicts with the hardware.

### Stroke Thickness vs. Cut Path
The laser follows the **centerline** of your vector. A thick visual stroke in the software can lead to "Kerf" errors (the width of the material removed by the laser).
* **Precision Tip:** Always set your stroke thickness to the minimum (e.g., 0.1mm). A thick 3mm stroke will cause the laser to cut significantly inside or outside the intended dimension, leading to a smaller or larger part than expected.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Comparison between Stroke Thickness and Actual Cut Path (Coming Soon)</figcaption>
</figure>

---

## Misalignment Between Engraving and Cutting

If your engraving shifts out of alignment with the final cut, it is rarely a hardware defect. Usually, it is a matter of **Motor Engagement**:

1.  **Motor Release:** By default, the system may release the stepper motors between tasks. If the carriage is bumped or moves slightly, the next layer will be offset.
2.  **The Solution:** Lock the motors via the **Control Bar** in Due Studio. Use the "Sensors and Actuators" toggle to keep the axes engaged throughout the entire multi-stage process.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 2: Engaging Motor Locks in Due Studio (Coming Soon)</figcaption>
</figure>

---

## Double Passes on the Same Line

If the laser passes over the same area twice, check for these two common vector errors:

### Overlapping Objects
You may have accidentally duplicated a layer. Click and drag the object; if an identical copy remains underneath, delete the duplicate before hitting **Due It!**.

### "Outline to Path" Conversion
There is a significant technical difference in how vectors are processed:
* **Standard Path:** The laser follows a single line once.
* **Outline to Path:** The software converts a line into a very thin "rectangle" or closed shape. The laser will then trace both sides of that thin line, effectively doubling the heat and the time spent on that section.

Use the **Node Editor** to verify if your lines are single paths or closed loops.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 3: Identifying Single Paths vs. Outlined Paths (Coming Soon)</figcaption>
</figure>

---

!!! info "Technical Support"
    If these adjustments do not resolve the discrepancy, you might be experiencing "Step Loss." Please contact **Due Laser Support** so we can help you fine-tune your motion parameters.