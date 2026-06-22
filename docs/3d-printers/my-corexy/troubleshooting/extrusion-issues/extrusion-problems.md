# General Extrusion Problems

!!! abstract "The Problem"
    This guide addresses the fundamental problem where filament is not coming out of the nozzle at all, or is extruding very inconsistently. You might hear a clicking or grinding sound from the extruder, or the printer might be moving and "printing" in mid-air.

<figure markdown="1">
  ![Common extrusion failure points](/images/image-placeholder.png#only-light){ width="600" }
  ![Common extrusion failure points](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>An illustration of common extrusion failure points: a clogged nozzle, heat creep in the heatbreak, and a grinding extruder gear.</figcaption>
</figure>

## Common Causes and How to Fix Them

If filament isn't coming out, there's a blockage or a failure somewhere in the path from the spool to the nozzle tip.

### 1. Clogged Nozzle

This is the most frequent issue. Debris, dust, or carbonized filament can create a blockage inside the nozzle.

* **Solution: Cold Pull.** A "cold pull" (or "atomic pull") is a highly effective cleaning method. Heat the nozzle to printing temperature, manually push some filament through, then let the nozzle cool down to around 80-90°C for PLA. Once at that temperature, pull the filament firmly and quickly out of the hotend. It should come out with a perfect mold of the nozzle's interior, pulling the debris out with it.
* **Solution: Nozzle Cleaning Needle.** Use a thin acupuncture needle (often included with printers) to carefully poke up through the nozzle tip while it's hot to dislodge any obstruction.

### 2. Extruder Clicking or Grinding

The clicking sound is the extruder's stepper motor skipping steps because it's trying to push filament but can't overcome the resistance. Grinding is when the extruder's gear strips away the filament instead of gripping it.

* **Solution:** First, assume you have a clog and address that (see cause #1). If the nozzle is clear, check the extruder itself.
    * **Clean the Gear:** The hobbed gear in the extruder can get clogged with plastic shavings. Use a small brush to clean its teeth.
    * **Check Tension:** The extruder arm has a spring that applies tension. If it's too loose, it won't grip the filament. If it's too tight, it will deform and grind the filament. Adjust the tension screw so the gear has a firm grip without crushing the filament.

### 3. Heat Creep

Heat from the heater block travels too far up the hotend's "heatbreak" (the transition tube), softening the filament before it reaches the melt zone. This soft filament then jams the path.

* **Cause:** The hotend's cooling fan (the one that is always on, pointing at the heatsink) is failing, blocked with dust, or not spinning fast enough.
* **Solution:** Ensure the hotend cooling fan is running at 100% speed whenever the hotend is hot. Clean any dust from the fan blades and the heatsink fins.

### 4. Broken Extruder Arm

On many entry-level printers, the extruder assembly is made of plastic. The tension arm is under constant pressure and is notorious for cracking, often in a place that's hard to see.

* **Solution:** Carefully remove and inspect the extruder arm, especially underneath. If you see a crack, even a hairline one, it needs to be replaced. It is highly recommended to upgrade to a metal extruder assembly, which is a cheap and very reliable upgrade.

## Quick Checklist
- [ ] Try to manually push filament through the hot nozzle. Does it flow?
- [ ] Perform a "cold pull" to clean the nozzle.
- [ ] Listen for extruder clicking and check the gear for plastic shavings.
- [ ] Inspect the extruder arm for cracks.
- [ ] Verify that the hotend's cooling fan is spinning correctly.