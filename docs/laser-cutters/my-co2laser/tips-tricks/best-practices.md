# Best Practices for Efficient Cutting

This guide outlines the essential procedures to ensure your **Neon** delivers high-quality cuts, maintains high productivity, and extends the lifespan of its components.

---

## I. Focal Point Precision

Laser cutting is only effective when the beam is perfectly focused. Think of it as a magnifying glass concentrating sunlight: the energy must converge at a single point to penetrate the material.

* **Adjustment:** Always use the official focus gauge to set the distance between the nozzle and the material.
* **Material Leveling:** Ensure your material is perfectly flat. If the honeycomb bed or the material itself is warped, the laser will be in focus in some areas and out of focus in others, leading to incomplete cuts.

---

## II. Optical Hygiene (Cleaning)

The **Neon's** laser beam is invisible and travels through a series of mirrors and lenses. Any dust or residue on these surfaces will absorb laser energy, reducing cutting power and potentially damaging the optics.

1.  **Laser Tube Output Lens:** Clean at least once a month. It is located at the exit of the glass tube.
2.  **Mirrors (1, 2, and 3):** Inspect daily. Mirror 3 (on the central carriage) is the most susceptible to smoke and requires frequent cleaning.
3.  **Focal Lens:** This is the closest component to the cutting area. Depending on the material (like MDF or Acrylic), you may need to clean both sides of the lens several times a day.

!!! tip "Cleaning Fluid"
    Use Isopropyl Alcohol and a lint-free microfiber cloth or optical swab. For stubborn residue, a drop of neutral detergent with warm water can be used before the final alcohol wipe.

---

## III. Parameter Testing

**IMPORTANT:** Never exceed 100% power in the software. Overloading the tube significantly reduces its lifespan. If a material isn't cutting, decrease the **Speed** instead of forcing higher power.

* **Test Patterns:** Before starting a project, cut small 1x1cm squares to find the ideal balance between speed and power. 
* **Consistency:** Keep a log of parameters for different materials to save time in future setups.

---

## IV. Cutting Order (Layer Management)

To ensure geometric precision, always prioritize **Internal Cuts** before **External Contours**.

* **The Logic:** If you cut the outer shape of a letter first, the piece might drop or shift slightly. If the internal holes (like the center of an "O") are cut afterward, they will be misaligned.
* **Neon Studio Tip:** Organize your work in layers. The **Neon** executes tasks from the top layer to the bottom layer in the list.

---

## V. Optical Path Alignment

The laser must hit the dead center of every mirror and the focal lens. If the beam is slightly off-course, you will lose power, especially at the far edges of the workbed. 
* Check your **Mirror Alignment** periodically, especially after moving the machine.

---

## VI. Laser Tube Lifespan

The laser tube is a consumable item. As the CO2 gas mixture depletes, you will notice a gradual need to decrease cutting speeds to achieve the same results.

* **Efficiency Monitoring:** If your production time is increasing significantly, it may be more cost-effective to replace the tube than to continue running at reduced speeds.
* **Visual Check:** A healthy tube glows with an intense magenta/pink light. A pale or white glow is a sign of gas depletion.

---

!!! info "Support"
    Do you have questions about a specific material or need help with calibration? Contact **Neon Laser Support**—we are here to help you succeed!