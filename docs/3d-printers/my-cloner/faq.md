# Frequently Asked Questions

This page answers common questions about the **My-Cloner Rev A**.

## What is the current hardware revision?

The current documented machine is **My-Cloner Rev A**.

Use the Rev A BOM, printed parts, wiring documentation and configuration files together. Do not mix older prototype parts or inherited MK3S instructions unless compatibility has been explicitly confirmed.

## What is the build volume?

The Rev A build volume is:

**230 × 230 × 220 mm**

## What electronics does the Rev A use?

The current architecture uses:

- MKS Robin Nano V3
- 5 × TMC2209 stepper drivers
- Raspberry Pi Zero 2 W
- LM2596 24 V → 5 V converter
- Klipper
- Mainsail

See [Wiring & Electronics](wiring/index.md) for the complete architecture.

## Does the My-Cloner use physical X and Y endstop switches?

No.

The Rev A uses **TMC2209 sensorless homing** on X and Y through StallGuard / DIAG.

The final sensitivity, motor current and homing-speed values are established during physical bring-up.

## Which Z probe is used?

The Rev A uses a **P.I.N.D.A. probe**.

The final controller input is still pending validation against the Rev A electrical schematic and physical machine.

## Which display is used?

The hardware includes an **MKS TS35 V2.0**.

Its final integration with the Klipper-based system is still under validation.

**Mainsail remains the primary user interface.**

## Which slicer should I use?

The recommended slicer is **OrcaSlicer**.

The final public Rev A profile package will be released after the profiles have been reviewed and tested on the physical machine.

See [Slicer Profiles](downloads/slicer-profiles.md).

## Where can I get the BOM?

The current BOM is available in the [Bill of Materials](bom/index.md) section and as downloadable XLSX / CSV files in [BOM Downloads](downloads/bom-files.md).

## Where can I get the STL files?

Use the current Rev A package from [STL Files](downloads/stl-files.md).

Do not mix printed parts from older revisions unless compatibility has been confirmed.

## Are CAD files available?

Yes. See [CAD Files](downloads/cad-files.md) for the currently available formats and project options.

## Is the final Klipper configuration available?

Not yet.

The final `printer.cfg` depends on physical validation of items including:

- Motor directions and currents
- X/Y sensorless homing
- P.I.N.D.A. input
- Fan assignment
- Thermistor models
- Heater parameters
- Filament sensor
- TS35 integration

See [Firmware Configuration](downloads/firmware-configuration.md).

## How do I perform the first power-on?

Follow the staged procedure in:

[Before First Power-On](operation/initial-setup/before-first-power-on.md)

and then:

[First Power-On](operation/initial-setup/first-power-on.md)

Do not jump directly to full homing or heater testing.

## How do I load or unload filament?

Follow:

[Loading and Unloading Filament](operation/initial-setup/loading-unloading-filament.md)

## What should I do if the printer reports a Klipper error?

Read the complete error in the Mainsail console first.

For hardware and communication issues, start with:

[Hardware Issues and Shutdowns](troubleshooting/hardware-issues.md)

## Where should I report a documentation problem?

If a page appears inconsistent with the current Rev A BOM, CAD, electrical schematic or validated firmware configuration, treat the engineering source as authoritative and report the documentation mismatch so it can be corrected.
