# Setting Up OrcaSlicer

**OrcaSlicer** is the recommended slicer for the **My-Cloner Rev A**.

The final public My-Cloner Rev A OrcaSlicer profile package is **not yet available**. It will be published after the machine, firmware-dependent settings and print profiles have been reviewed and tested.

!!! warning "Do Not Use Legacy My-Cloner Profiles"
    Older local or prototype profiles may contain settings inherited from other machines.

    Do not treat them as the final Rev A definition.

## Download and Install OrcaSlicer

Download OrcaSlicer from the official project releases:

[OrcaSlicer Releases](https://github.com/SoftFever/OrcaSlicer/releases){ target="_blank" rel="noopener noreferrer" }

Install the appropriate version for your operating system.

## Current Rev A Machine Baseline

Until the official package is released, the documentation baseline is:

| Setting | Rev A Definition |
|---|---|
| Printer | My-Cloner |
| Firmware | Klipper |
| Build volume | 230 × 230 × 220 mm |
| Standard nozzle | 0.4 mm |
| Host interface | Mainsail |
| Slicer | OrcaSlicer |

Firmware-dependent motion limits, start/end G-code, macros and tuned process values remain subject to Rev A physical validation.

## Official Profile Package

When released, the My-Cloner package will provide the reviewed printer definition and associated profile data required for the Rev A machine.

The download will be published in:

[Slicer Profiles](../downloads/slicer-profiles.md)

## Connecting OrcaSlicer to Mainsail

After Klipper and Mainsail are operational, OrcaSlicer can be configured to communicate with the printer over the network.

Use the printer's Mainsail / Moonraker address in OrcaSlicer's device connection settings.

!!! note "Connection Is Separate from the Printer Profile"
    A successful network connection does not validate the machine profile.

    The printer definition, firmware configuration and physical machine must all agree before a G-code file is considered suitable for the Rev A.

## Before the First Print

Before sending G-code from OrcaSlicer:

1. Complete the controlled Rev A bring-up.
2. Validate homing and motion.
3. Validate heaters, thermistors and fans.
4. Complete PID calibration.
5. Calibrate the P.I.N.D.A. Z offset and bed mesh.
6. Confirm the installed nozzle.
7. Review the generated G-code preview.

Continue with:

[Basic Slicing Workflow](basic-slicing-workflow.md)
