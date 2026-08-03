# Troubleshooting: Incomplete Cutting (Under-penetration)

If your **Neon** is firing the laser but the beam fails to cut completely through the material, the efficiency of the optical system or the parameter configuration is likely compromised. Use this guide to identify and resolve the most common causes of power loss.

---

## 1. Focal Inconsistency

The CO2 laser relies on an extremely precise focal point to concentrate energy. If the beam is "out of focus," the energy density scatters, resulting in thick, charred lines instead of a clean, deep cut.

* **Calibration:** Ensure you used the focus gauge correctly. Refer to our **Focus Adjustment** guide for the standard procedure.
* **Material Leveling:** If the cut fails only in specific areas of the workbed, the material may be warped or uneven. 
    * **Support Blades:** Verify that all support fins are properly seated and aligned.
    * **Honeycomb Bed:** Check for small debris or cutouts trapped under the bed that might be lifting the material.

---

## 2. Contamination of Optical Components

Preventive maintenance is vital. Dirty lenses and mirrors absorb laser energy (converting it into heat within the component) instead of transmitting it to the material.

* **Residue Buildup:** Smoke and resins from materials like MDF or acrylic deposit on the optics over time.
* **Cleaning Protocol:** Systematically clean the three mirrors and the focal lens.
    * **Important:** Do not forget the output lens of the laser tube itself, which can also accumulate dust or film.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Identifying Contamination on Optical Lenses (Coming Soon)</figcaption>
</figure>

---

## 3. Parameter Optimization

Finding the perfect balance between **Speed** and **Power** is an empirical process that depends on material density.

* **Density Variations:** Natural materials (like wood) have inconsistent densities. A setting that worked on one batch may require adjustment for the next.
* **Test Patterns:** Always run a parameter test jig before starting large-scale production. 
* **Power Decay:** If you are running at 100% power and very low speed without success, the material may be too dense for the **Neon's** rated capacity.

---

## 4. Optical Alignment (Mirror Synchronization)

If the laser loses strength as the head moves toward the right or the back of the machine, the mirrors are misaligned. This causes the beam to enter the lens off-center, losing energy as it strikes the internal walls of the nozzle.

* **Diagnosis:** Perform the pulse test at the four corners of the work area. If the marks do not coincide, refer to the **Mirror Alignment Manual**.

---

## 5. Hardware Integrity: Laser Tube Output

In rare cases, penetration failure is caused by a physical issue with the tube hardware:

* **Loose Output Coupler:** The metal tip at the end of the tube (where the final internal mirror is housed) can become detached due to vibrations or thermal cycles.
* **Inspection:** With the **Neon unplugged**, visually check if the metal coupler at the left end of the tube is firmly attached. Any play or gap will cause the beam to exit divergently.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 2: Inspecting the Laser Tube Output Head (Coming Soon)</figcaption>
</figure>

---

!!! danger "Safety First"
    Any physical intervention regarding the tube or mirror adjustments must be performed with proper eye protection. Ensure the machine is disconnected during manual inspections.

---
**Still experiencing cutting issues?**
Small calibration adjustments can transform your machine's performance. If the problem persists, contact **Due Laser Support** for a detailed technical analysis of your **Neon**.