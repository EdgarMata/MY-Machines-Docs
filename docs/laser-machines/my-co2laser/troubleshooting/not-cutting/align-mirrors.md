# Optical Path Calibration: Mirror Alignment

The laser beam travels from the tube and is redirected by three strategic mirrors before reaching the focus lens and the material. Ensuring these mirrors are perfectly synchronized is vital for consistent cutting power across the entire workbed.

---

## Understanding the Optical Path

If you notice that the **Neon** loses cutting efficiency on the right side of the machine, the mirrors likely require recalibration. Over time or after transportation, these components may shift slightly, causing the beam to diverge from its intended path.

<figure markdown="span">
  ![](../images/construcao-light.png#only-light){ width="400" }
  ![](../images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Diagram of the Neon Optical Path (Coming Soon)</figcaption>
</figure>

---

## Lateral Mirror Alignment Verification

This test determines if the first and second mirrors are projecting the beam parallel to the motion axes.

### Required Materials
* Adhesive paper labels or masking tape.

### Step-by-Step Diagnostic
1.  **Prepare the Target:** Apply four layers of masking tape over the laser entry port on the carriage.
2.  **Left-Side Pulse:** Position the laser head at the far **left** of the work area. Use the **Neon** software (Due Studio) to fire a short "Pulse" (Pulse/Fire button).
3.  **Analyze the Mark:** The laser will leave a small burn mark on the tape. **Do not remove the tape yet.**
4.  **Right-Side Pulse:** Move the carriage to the far **right** of the machine. Fire a second short pulse.

<figure markdown="span">
  ![](../images/construcao-light.png#only-light){ width="400" }
  ![](../images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Video: Testing Mirror Convergence (Coming Soon)</figcaption>
</figure>

### Evaluation
* **Aligned:** Both pulses hit the exact same spot on the tape.
* **Misaligned:** You see two distinct marks or the second pulse hits the edge of the port. This confirms the lateral mirrors need adjustment.

---

## Central Mirror (Third Mirror) Verification

If the lateral alignment is perfect but the cut quality is still poor, the third mirror (located inside the central carriage) might be misdirected, causing the beam to hit the internal walls of the nozzle.

1.  **Nozzle Target:** Place a piece of tape over the bottom exit of the laser nozzle. Press it gently to mark the nozzle's circumference on the tape.
2.  **Fire Pulse:** Execute a short pulse through the software.
3.  **Inspect Centering:** Remove the tape and check the position of the burn mark relative to the circular indentation of the nozzle.

!!! tip "Optimal Result"
    The pulse must be perfectly centered. If the mark is near the edge, the laser is losing energy through thermal dissipation against the nozzle walls, significantly reducing cutting power.

<figure markdown="span">
  ![](../images/construcao-light.png#only-light){ width="400" }
  ![](../images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 2: Centered vs. Off-center Beam Comparison (Coming Soon)</figcaption>
</figure>

---

## Maintenance and Efficiency

If the alignment appears correct but efficiency is still low, consider these factors:
* **Distance Factor:** Naturally, the beam loses a negligible amount of intensity as the path lengthens. To minimize this, ensure your optics are spotless.
* **Component Hygiene:** Accumulation of dust or resin on mirrors and lenses is the most common cause of power loss. Refer to our guides on **Lens Maintenance** and **Mirror Cleaning**.

---

!!! danger "Precision Calibration"
    Operating the **Neon** with misaligned optics can cause overheating of the internal components. If the pulses do not coincide, proceed immediately to the **Mirror Adjustment Guide**.

---
**Need Technical Guidance?**
Optical alignment requires precision. If you are unable to center the beam, contact **Due Laser Support** for a guided calibration session.