# Skipped Layers and Gaps

The term "skipping layers" often describes a print defect where it appears that one or more entire layers are missing, leaving visible horizontal gaps in the model and making it extremely weak.

!!! info "Is it a Z-axis problem or an extrusion problem?"
    While it might look like the Z-axis failed to move up, this issue is almost always a severe case of **under-extrusion**. The printer *did* move up to the next layer, but it failed to extrude any plastic (or extruded very little) for that period.

---
### Primary Cause: Severe Under-Extrusion

This problem shares all the same causes as regular under-extrusion. The issue has simply become so severe that extrusion stops completely for a short time.

The most common culprits are:

* **A Partially or Fully Clogged Nozzle:** Debris inside the nozzle is preventing the flow of plastic.
* **A Dirty Extruder Drive Gear:** The gear that pushes the filament is slipping because its teeth are clogged with plastic shavings.
* **Heat Creep:** Heat is traveling too far up the hotend, causing the filament to soften prematurely and jam before it reaches the melt zone. This is often caused by a failing hotend fan.
* **Incorrect Temperature:** The printing temperature is too low for the filament, making it too viscous to be extruded properly.

!!! success "How to Fix It: See the Under-Extrusion Guide"
    Because this is an extrusion issue, the solutions are covered in detail in a separate guide.

    **➡️ Please refer to the `Troubleshooting: Under-extrusion` guide for a complete step-by-step list of solutions.**
