# Under-Extrusion

!!! abstract "The Problem"
    **Under-extrusion** occurs when the printer fails to extrude the correct amount of material. It's extruding, but not enough. This results in prints that are weak, flimsy, and have characteristic gaps between layers and walls, or even entire missing layers.

<figure markdown="1">
  ![A print showing signs of under-extrusion](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![A print showing signs of under-extrusion](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>A 3D print, like a calibration cube, showing classic signs of under-extrusion: gaps between walls, holes in the top surface, and an overall flimsy appearance.</figcaption>
</figure>

## Common Causes and How to Fix Them

Under-extrusion means the printer thinks it's pushing enough filament, but reality doesn't match the expectation.

### 1. Incorrect Flow Rate / Extrusion Multiplier

This is a slicer setting that acts as a fine-tuning knob for extrusion. If it's set too low, the slicer will command less material flow than needed.

* **Solution: Calibrate Flow Rate.** The most reliable method is to print a hollow, single-wall cube with no top layers. Use calipers to measure the thickness of the wall. If you requested a 0.4mm wall and it measures 0.35mm, you are under-extruding. You can calculate the new flow rate with `(Expected thickness / Actual thickness) * Current Flow Rate`. Adjust the `Flow Rate` (or `Extrusion Multiplier`) in your slicer accordingly.

### 2. Uncalibrated E-Steps

This firmware value tells the printer how many "steps" the extruder motor needs to turn to push 1mm of filament. If this value is wrong, all extrusion will be off.

* **Solution: Calibrate E-Steps.** This involves telling the printer to extrude 100mm of filament and measuring how much it actually extruded. There are many excellent online guides for "E-step calibration." It's a fundamental calibration that, once set, rarely needs to be changed.

### 3. Partial Nozzle Clog

A small piece of debris can partially block the nozzle, restricting flow but not stopping it completely.

* **Solution:** A partial clog can often be cleared by a "cold pull". If the problem persists, the nozzle might need a more thorough cleaning or replacement. Refer to the [General Extrusion Problems](./extrusion-problems.md) guide.

### 4. Printing Too Fast (Exceeding Volumetric Flow)

Your hotend has a maximum speed at which it can melt plastic. If you tell it to print faster than this limit, the filament passes through without fully melting, causing resistance and leading to under-extrusion.

* **Solution:** Simply try reducing your overall print speed by 20-30% and see if the problem improves. If it does, you have found your hotend's performance limit.

## Quick Checklist
- [ ] Calibrate your `Flow Rate` / `Extrusion Multiplier` in the slicer.
- [ ] Perform an E-step calibration for your extruder.
- [ ] Check for and clean any partial nozzle clogs.
- [ ] Reduce your print speed to see if the hotend is the bottleneck.
- [ ] Check that the filament diameter in your slicer matches your filament (e.g., 1.75mm).
