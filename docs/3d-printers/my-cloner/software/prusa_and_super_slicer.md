# PrusaSlicer & SuperSlicer

The recommended slicer for the **My-Cloner Rev A** is **OrcaSlicer**.

PrusaSlicer and SuperSlicer can be configured for a Klipper printer, but **official validated My-Cloner Rev A profile bundles for these slicers are not currently published**.

## Current Project Position

The Rev A release work is focused on:

- A validated My-Cloner machine definition
- OrcaSlicer printer settings
- Tested filament and process profiles
- Klipper / Mainsail workflow

Do not import profile bundles from older My-Cloner prototypes or unrelated MK3/MK3S configurations and assume that they are compatible.

## Using Another Slicer

If you choose to configure PrusaSlicer or SuperSlicer manually, the machine definition must agree with the validated My-Cloner Rev A configuration, including:

- Build volume: 230 × 230 × 220 mm
- 0.4 mm standard nozzle
- Klipper-compatible G-code workflow
- Current motion limits
- Current start/end G-code or macros
- Validated material settings

Motion limits, machine G-code and other firmware-dependent values must not be copied from a legacy printer profile before the final Rev A Klipper configuration has been validated.

## G-Code Transfer

Generated G-code can be exported from the slicer and uploaded to **Mainsail**.

Always review the sliced file before printing and never run G-code prepared for a different machine unless its compatibility has been verified.

## Related Documentation

For the recommended slicer:

[Setting Up OrcaSlicer](setting-up-orca-slicer.md)

For the current public-profile status:

[Slicer Profiles](../downloads/slicer-profiles.md)
