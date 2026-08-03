# Solving Extrusion Problems

Problems like "clogs," "jams," and filament "grinding" are some of the most common issues in 3D printing. They all share the same root cause: for some reason, the filament cannot be pushed through the hotend correctly. This guide provides a step-by-step diagnostic, from the easiest to the most complex fixes.

!!! info "Symptoms of Extrusion Problems"
    * The printer is moving, but no plastic is coming out of the nozzle.
    * The plastic extrudes very thinly or inconsistently (signs of a **partial clog**).
    * You hear a clicking or ticking sound from the extruder, which is the motor trying to push the filament but failing.
    * You hear a grinding sound, and you find the filament has been chewed through by the extruder gear.

---
### Step 1: Check the Basics (The Easy Stuff)

Before disassembling anything, check these simple settings.

* **Is the temperature correct?**
    * **Problem:** Every filament has an ideal printing temperature. If the nozzle is too cold, the plastic will be too viscous to flow properly, causing a jam.
    * **Solution:** Double-check that you have selected the correct material profile in your slicer and that the nozzle temperature matches the filament manufacturer's recommendation.

* **Is the nozzle too close to the bed?**
    * **Problem:** On the first layer, if the nozzle is too close to the print bed, the opening is blocked. The extruder has nowhere to push the plastic, leading to a jam and filament grinding right at the start of a print.
    * **Solution:** Re-run your "First Layer Calibration" and ensure the "Live Adjust Z" is set correctly. The nozzle should be close enough for adhesion but high enough to allow a smooth flow of plastic.

---
### Step 2: Clear a Partial Clog

If filament is still coming out, but it's thin or inconsistent, you likely have a partial clog.

* **Solution: Use a Cleaning Needle**
    1.  Heat the nozzle to the printing temperature of the material that is stuck.
    2.  Carefully insert the thin cleaning needle (acupuncture needle) that came with your printer into the tip of the nozzle from below.
    3.  Push it in about 1-2 cm and move it around gently.
    4.  Remove the needle and extrude some filament. Repeat until the flow is smooth and consistent.

    <figure markdown="1">
      ![Nozzle Needle Cleaning](/assets/images/image-placeholder.webp#only-light){ width="600" }
      ![Nozzle Needle Cleaning](/assets/images/image-placeholder.webp#only-dark){ width="600" }
      <figcaption>Illustration of a cleaning needle being inserted into the tip of a hot nozzle.</figcaption>
    </figure>

* **Advanced Solution: The "Cold Pull"**
    For more stubborn clogs, search online for a guide on how to perform a "Cold Pull" or "Atomic Pull." This technique involves pushing filament through a hot nozzle, letting it cool slightly, and then pulling it back out, dragging the debris with it.

---
### Step 3: Check the Extruder Mechanism

If you hear grinding noises and see chewed-up filament, the problem is at the extruder itself.

* **Problem: Dirty Drive Gear**
    * **Cause:** The toothed gear that grips the filament can get clogged with plastic shavings, causing it to lose its grip and grind the filament instead of pushing it.
    * **Solution:** Clean the gear's teeth with a small brass brush and a toothpick. See the `Cleaning the Extruder (Drive Gear)` guide for details.

* **Problem: Incorrect Idler Tension**
    * **Cause:** The "idler" is the part that presses the filament against the drive gear. If the tension is too loose, the gear won't grip. If it's too tight, it can deform the filament and cause it to get stuck further down the hotend.
    * **Solution:** Adjust the tension screw for the extruder's idler door. It should be tight enough to provide a firm grip without crushing the filament.

---
### Step 4: Full Hotend Disassembly (Major Jam)

!!! danger "Last Resort"
    If none of the above steps work, you may have a severe jam inside the hotend. This could be a piece of broken filament or a deformed PTFE tube. This requires disassembling the hotend.

* **Solution:** Follow the reactive maintenance guides for `Replacing the Nozzle` and `Replacing the Hotend PTFE Tube`. This will allow you to fully inspect and clear the filament path.

<figure markdown="1">
  ![Extrusion Problems](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Extrusion Problems](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>Illustration of common extrusion problems like clogs, jams, and grinding.</figcaption>
</figure>
