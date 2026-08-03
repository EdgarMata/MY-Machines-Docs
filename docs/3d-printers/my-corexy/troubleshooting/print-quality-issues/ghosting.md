# Ghosting (Ringing)

!!! abstract "The Problem"
    **Ghosting** (also known as **ringing** or echoing) is a visual artifact that manifests as ripples on the surface of the print, appearing immediately after corners or sharp details. It's an echo of the printer's vibration.

<figure markdown="1">
  ![A 3D print showing ghosting artifacts](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![A 3D print showing ghosting artifacts](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>A 3D print showing ghosting artifacts, which look like ripples or echoes, appearing after sharp corners or details.</figcaption>
</figure>

## Common Causes and How to Fix Them

Ghosting is almost always caused by vibrations. The print head moves and stops abruptly, but inertia causes the printer's frame to continue vibrating for a fraction of a second, and this vibration is "printed" onto the part.

### 1. Excessive Speed and Acceleration

This is the most common cause. You are asking your printer to change direction faster than its mechanical frame can handle without vibrating.

* **Simple Fix:** Lower the print speed in your slicer, especially the `Outer Wall Speed`. Reducing the overall speed to 40-50mm/s often solves the problem.
* **Advanced Fix:** Lower the `Acceleration` and `Jerk` (or `Junction Deviation`) values in your slicer or printer firmware. Lower acceleration smooths out direction changes.

### 2. Mechanical Tension Issues

Loose belts or loose components allow vibrations to propagate and are not dampened correctly.

* **Solution:**
    * **Tighten Belts:** Check the tension of the X and Y-axis belts. They should be taut, emitting a low bass note when plucked, but not so tight that they restrict movement.
    * **Check Pulleys:** Confirm that the small pulleys attached to the stepper motor shafts are tight. Check that the grub screws are firm against the flat part of the motor shaft.
    * **Check Wheels:** Ensure that the wheels running on the aluminum extrusions are snug, with no wobble.

### 3. External Vibrations

The surface the printer is sitting on may be amplifying the vibrations.

* **Solution:** Place the printer on a very heavy and stable surface (a sturdy workbench, or even the floor).
* **Popular Solution:** Place a concrete paving slab with a foam mat underneath the printer. The mass of the slab absorbs high-frequency vibrations.

## Quick Checklist
- [ ] Lower the print speed and acceleration.
- [ ] Check the tension of the X and Y-axis belts.
- [ ] Tighten the motor pulley grub screws.
- [ ] Ensure the printer is on a stable, heavy surface.
