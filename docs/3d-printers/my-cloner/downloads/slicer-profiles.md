# Slicer Profiles

MyMachines provides dedicated **OrcaSlicer** profiles for the My-Cloner and other MyMachines printers.

A My-Cloner profile set already exists and includes machine definitions, printable-bed assets and print-process profiles for multiple nozzle sizes.

However, the current profiles are being reviewed and updated for the **My-Cloner Rev A** hardware and Klipper configuration.

!!! warning "Rev A Profiles Under Validation"
    The existing My-Cloner profiles were developed from an earlier configuration and still contain legacy settings inherited from previous printer definitions.

    They should **not yet be considered the final My-Cloner Rev A profiles**.

## Current Profile Structure

The My-Cloner profile set currently includes machine configurations for:

| Nozzle | Status |
|---|---|
| **0.2 mm** | Existing profile — validation required |
| **0.4 mm** | Existing profile — validation required |
| **0.6 mm** | Existing profile — validation required |
| **0.8 mm** | Existing profile — validation required |

The standard My-Cloner Rev A nozzle is:

**0.4 mm**

Multiple print-process profiles also exist for different layer heights and printing priorities, including detail, quality, standard, speed and draft profiles.

## OrcaSlicer

The recommended slicer for the My-Cloner is:

**OrcaSlicer**

The long-term goal is to maintain a complete **MyMachines vendor profile** so MyMachines printers can be selected and configured directly through OrcaSlicer.

## Rev A Update

Before the profiles are released as official My-Cloner Rev A profiles, they will be reviewed against the final machine configuration.

The review includes:

- Build volume
- Printable area
- Nozzle configuration
- Maximum speeds
- Acceleration limits
- Klipper G-code
- Start G-code
- End G-code
- Bed model and texture
- Filament compatibility
- Print-process profiles

Legacy Prusa- and MK3-specific commands and identifiers will be removed where they are not applicable to the My-Cloner Rev A.

!!! info "Klipper Configuration Dependency"
    The final OrcaSlicer profiles will be validated together with the official My-Cloner Rev A Klipper configuration.

    This ensures that slicer commands, motion limits and printer macros match the actual `printer.cfg`.

## Download

The final My-Cloner Rev A OrcaSlicer profile package is **not yet available for public download**.

The download will be added here after the profiles have been reviewed and tested on the Rev A machine.

## Related Documentation

For the future Klipper configuration:

[Firmware Configuration](firmware-configuration.md)

For the standard printer specifications:

[Bill of Materials](bom-files.md)

For printable parts:

[STL Files](stl-files.md)
