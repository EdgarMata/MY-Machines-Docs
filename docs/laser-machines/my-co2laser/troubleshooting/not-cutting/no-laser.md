# Troubleshooting: No Laser Emission

If your **Neon** is performing the X and Y axis movements but there is no laser beam output or the material is not being marked, the issue may range from software configurations to failures in the safety or optical systems. Follow this progressive diagnostic protocol.

---

## 1. Power Parameter Verification (Software)

This is the most frequent scenario: the machine simulates the job, but the laser intensity is insufficient to cause a thermal reaction in the material.

* **Ignition Threshold:** CO2 laser tubes have a minimum power requirement to "fire" (typically between 8% and 12%). If your project is configured with values below this, the gas will not ionize.
* **Diagnostic Test:** Create a small square in **Due Studio** and run it with **Power at 35%** and **Speed at 20**. 
    * **If it works:** The issue was simply the parameter configuration for that specific material. Adjust your cutting tables accordingly.

---

## 2. Safety System and Cooling Flow

The **Neon** features a **Flow Sensor** that acts as a safety interlock. If the system detects that the coolant is not circulating, the laser is instantly disabled to prevent the tube from exploding due to thermal shock.

* **Hose Obstruction:** Check if the silicone hoses are kinked or "strangled" at any point along the path.
* **Reservoir Level:** Ensure the water reservoir is filled to the appropriate level (above the pump).
* **Pump Operation:** Visually verify if water is entering the laser tube (check for persistent air bubbles) or feel the mechanical vibration in the outlet hose.

!!! info "Safety Note"
    Never attempt to bypass the flow sensor. Operating the tube without active cooling will cause irreversible damage within seconds.

---

## 3. Optical Path Integrity (Alignment)

If you can see a magenta/pink glow inside the tube, but the laser doesn't reach the material or arrives very weak, the problem lies in **mirror misalignment**.

* **Beam Deviation:** The laser might be firing, but striking the metal guards or the internal wall of the nozzle due to misalignment.
* **Procedure:** Consult our **Optical Path Calibration** guide to verify if the pulses coincide at the extreme points of the work area.

---

## 4. Optical Maintenance (Lenses and Mirrors)

Accumulated debris (soot or resin) on the mirrors or the focal lens can absorb the laser energy instead of reflecting or transmitting it.

* **Visual Inspection:** Check for opaque spots or charred residue on the final lens. A dirty lens can reduce cutting efficiency by up to 80%.

---

!!! danger "Advanced Diagnostics"
    If after checking the power, water flow, and alignment, the **Neon** still fails to emit a laser beam, the issue may reside in the **High Voltage Power Supply (PSU)** or the **Laser Tube** itself. 

---
**Need Technical Support?**
If the steps above do not resolve the fault, do not hesitate to contact the **Due Laser** specialist team. We are available through official channels to perform a detailed remote diagnostic of your **Neon**.