# Over-extrusion

Over-extrusion occurs when the printer pushes out more plastic than necessary, resulting in parts with excess material, rough surfaces, and dimensional inaccuracy.

### Common Symptoms

* The top surface of the print is not smooth, but rough and bumpy.
* The part's dimensions are slightly larger than expected.
* The nozzle drags material as it moves over the part.
* Blobs or zits of material on the walls of the print.

### Solutions

1.  **Calibrate the Flow Rate**
    !!! success "Primary Solution"
        The most common cause is a Flow Rate (also known as "Extrusion Multiplier") that is set too high.
        * **During the Print:** You can make a quick adjustment in the printer's menu. Look for the `Tune -> Flow` option and reduce the value in small steps (e.g., from 100% to 98% or 95%).
        * **In the Slicer:** For a permanent fix, adjust the "Extrusion Multiplier" or "Flow" setting in your filament's profile in your slicing software.

2.  **Check Filament Diameter in Slicer**
    Ensure that the filament diameter configured in your slicing software matches the actual diameter of the filament you are using (usually 1.75 mm). If the slicer thinks it's using a thinner filament, it will push out more material.

3.  **Over-extrusion on the First Layer**
    If the problem only occurs on the first layer (similar to "Elephant Foot"), the cause is likely a nozzle that is too close to the bed. Adjust your "Live Adjust Z" to a less negative value.