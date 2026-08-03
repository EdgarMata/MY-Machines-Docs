# Layer Shifting

!!! abstract "The Problem"
    **Layer shifting** is a dramatic printing failure where the layers of a print become misaligned along the X or Y axis. The printer loses its intended coordinates, resulting in a distinct "stair-step" effect that ruins the part.

<figure markdown="1">
  ![A 3D print showing a severe layer shift](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![A 3D print showing a severe layer shift](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>A 3D print exhibiting a severe layer shift, where the upper layers have been abruptly misaligned from the bottom layers along the X or Y axis.</figcaption>
</figure>

## Common Causes and How to Fix Them

Layer shifting means the printer's control board thinks the print head is in one position, but it's actually in another. This is almost always caused by the motor being unable to complete a commanded move.

### 1. Loose Belts or Pulleys (Most Common Cause)

If a belt is loose, the motor turns its pulley, but the belt slips instead of moving the print head or bed the full, precise distance. A pulley that is loose on the motor shaft has the same effect.

* **Solution:**
    * **Tighten Belts:** Check the tension of your X-axis (print head side-to-side) and Y-axis (bed front-to-back) belts. They should be taut, like a low-pitched guitar string. They should not droop, but also should not be so tight that they restrict movement. Adjust the belt tensioners on your printer as needed.
    * **Check Pulleys:** Find the small gear-like pulleys on the stepper motor shafts. Ensure the small set screws (grub screws) are tight. It is crucial that one of the grub screws is tightened against the flat spot on the motor shaft to prevent any slipping.

### 2. Printing Speed or Acceleration is Too High

If you command the printer to move or change direction too quickly, the stepper motors may not have enough torque to execute the move, causing them to "skip steps" and lose their position.

* **Solution:** Reduce your `Print Speed`, `Travel Speed`, and especially the `Acceleration` settings in your slicer. Try lowering acceleration to a conservative value like 500 mm/s² and see if the problem disappears.

### 3. Mechanical Obstruction or Binding

Something is physically preventing the print head or bed from moving freely. The motor tries to push past the obstruction, skips steps, and the shift occurs.

* **Solution:** With the printer's motors disabled, manually and slowly move the print head along the X-axis and the bed along the Y-axis. Feel for any spots where it gets stuck, binds, or requires more force. Look for cables that might be snagging, binder clips holding the build plate that might be hitting the frame, or debris on the guide rails.

### 4. Overheating Stepper Motor Drivers

The small driver chips on the mainboard that control the motors can overheat, especially during long prints in a warm environment or enclosure. When they overheat, they can temporarily shut down to protect themselves, causing the motor to miss steps.

* **Solution:** Ensure the fan cooling the mainboard is working correctly and that there is adequate airflow over the control board. If the driver chips have heatsinks, make sure they are securely attached.

## Quick Checklist
- [ ] Check and tighten X and Y-axis belts.
- [ ] Check and tighten the grub screws on the motor pulleys.
- [ ] Reduce print speed and acceleration settings in your slicer.
- [ ] Manually move the axes to check for any binding or obstructions.
- [ ] Verify that the mainboard cooling fan is operational.

