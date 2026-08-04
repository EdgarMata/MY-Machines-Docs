# Warping

!!! abstract "The Problem"
    **Warping** happens when the corners of a 3D print contract, curl upwards, and detach from the print bed during the process. It's more common with large parts and high-shrinkage materials like ABS.

<figure markdown="1">
--8<-- "image-placeholder.md"
  <figcaption>A 3D print with its corners lifting off the print bed, a clear example of warping.</figcaption>
</figure>

## Common Causes and How to Fix Them

Warping is a problem of **thermal contraction**. As hot plastic cools, it shrinks. The upper layers cool and contract, exerting a pulling force on the bottom layers, which are stuck to the bed. If this pulling force is greater than the bed adhesion force, the corners lift.

### 1. Poor Bed Adhesion

If the first layer isn't perfectly stuck, any small contraction force will be enough to lift it.

* **Fix 1: Cleanliness:** The most common cause of poor adhesion is a dirty bed. Clean it with Isopropyl Alcohol (IPA >90%) before every print to remove grease and dust.
* **Fix 2: Leveling and Z-Offset:** Ensure your [first layer is perfect](../../tips-and-tricks/perfect-first-layer.md). The nozzle must be close enough to the bed to slightly "squish" the filament, maximizing contact.
* **Fix 3: Bed Temperature:** Use the recommended bed temperature for your material (60°C for PLA, 70-85°C for PETG, 100-110°C for ABS). This keeps the bottom layers of plastic above their "glass transition temperature," making them less prone to shrinking.

### 2. Rapid and Uneven Cooling

Drafts or excessively fast cooling of the upper layers accelerate contraction, increasing the pulling forces.

* **Fix 1: Brim or Raft:** In your slicer, add a "Brim." This flange around the base of the part increases the first layer's surface area, fighting the lifting force. A "Raft" is a more extreme but also effective solution.
* **Fix 2: Turn Off the Fan:** Program the slicer to keep the part cooling fan off for the first 5 to 10 layers.
* **Fix 3: Use an Enclosure:** This is the ultimate solution, especially for ABS/ASA. An enclosure keeps the ambient air temperature around the part high and stable, drastically minimizing thermal contraction.

### 3. Part Geometry

Sharp 90-degree corners concentrate contraction stresses.

* **Fix:** If you are designing the part, add a small rounded corner ("fillet") to the base. This helps to distribute the forces more evenly.

## Quick Checklist
- [ ] Clean the print bed with Isopropyl Alcohol.
- [ ] Check bed leveling and Z-Offset height.
- [ ] Increase bed temperature by 5°C.
- [ ] Add a 5 to 10mm Brim in the slicer.
- [ ] Turn off the part cooling fan for the first few layers.
- [ ] Use an enclosure to block drafts (essential for ABS/ASA).
