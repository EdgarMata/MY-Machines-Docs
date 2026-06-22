# Layer Shifting and Misalignment

Layer shifting is a printing failure where one or more layers are suddenly offset from the rest of the print, creating a "staircase" effect where the walls should be smooth. This ruins the print's dimensional accuracy and appearance.

!!! info "What causes layer shifting?"
    This issue is almost always caused by a mechanical problem that prevents the print head or the bed from moving to its intended position for a moment. The printer's motors "skip" steps, and the printer continues the print from this new, incorrect position.

---
### Primary Mechanical Causes

These are the most common reasons for layer shifting and should be the first things you check.

1.  **Loose Belts (X or Y Axis)**
    * **Problem:** If a belt on the X-axis (which moves the print head left-to-right) or the Y-axis (which moves the bed front-to-back) is loose, it can slip on the motor pulley, causing the printer to lose its position.
    * **Solution:** Check the tension of both belts. They should be taut enough to make a low-pitched "twang" when plucked, but not so tight that they restrict movement. Refer to the `Checking and Adjusting Belt Tension` guide for details.

    <figure markdown="1">
      ![Belt Tension Check](/images/image-placeholder.png#only-light){ width="600" }
      ![Belt Tension Check](/images/image-placeholder.png#only-dark){ width="600" }
      <figcaption>Illustration comparing a properly taut belt versus a visibly loose and sagging belt.</figcaption>
    </figure>

2.  **Loose Pulley on Motor Shaft**
    * **Problem:** The pulley is the toothed gear attached directly to the motor shaft, which drives the belt. It is secured by one or two small screws called "grub screws." If these screws are loose, the motor shaft can spin inside the pulley, leading to lost motion.
    * **Solution:** Ensure the pulley's grub screw is tightened securely against the **flat side** of the motor shaft. This flat spot ensures the screw has a solid surface to lock onto and cannot slip.

    <figure markdown="1">
      ![Pulley Grub Screw](/images/image-placeholder.png#only-light){ width="600" }
      ![Pulley Grub Screw](/images/image-placeholder.png#only-dark){ width="600" }
      <figcaption>A close-up illustration of a motor shaft with its flat side, and an arrow pointing to the grub screw on the pulley that must be tightened against it.</figcaption>
    </figure>

### Other Causes and Solutions

* **Print Collisions:** If the nozzle physically collides with the print, it can be forceful enough to cause the motor to skip steps. This often happens if a part of the print has curled up due to **warping**.
    * **Solution:** Resolve any warping issues first. See the `Troubleshooting: Warping` guide.

* **Printing Speed Too High:** Excessively high print or travel speeds increase the forces on the motors and the likelihood of skipping steps if there is any resistance.
    * **Solution:** Try reducing the print and travel speeds in your slicer settings.

* **Firmware Crash Detection:**
    !!! tip "Use Crash Detection"
        Some printers have a "Crash Detection" feature that can detect skipped steps and attempt to pause or recover. [cite_start]This feature typically only works in "Normal" or "Loud" mode, not in "Stealth" or "Quiet" mode. [cite: 482]

<figure markdown="1">
  ![Layer Shifting Example](/images/image-placeholder.png#only-light){ width="600" }
  ![Layer Shifting Example](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of a print with misaligned layers.</figcaption>
</figure>