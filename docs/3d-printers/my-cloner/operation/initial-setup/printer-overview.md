# My-Cloner Printer Overview

Welcome to the **My-Cloner** initial setup guide.

This page introduces the main parts of the printer and explains the basic machine architecture before you begin the first setup and calibration procedures.

!!! info "Hardware Revision"
    This documentation refers to **My-Cloner Rev A**.

---

## About the My-Cloner

The My-Cloner is an open-source Cartesian FDM 3D printer developed by **MyMachines**.

The current Rev A machine uses:

- 24 V electrical architecture
- Klipper firmware
- MKS Robin Nano V3.0 mainboard
- Raspberry Pi Zero 2 W as the Klipper host
- Mainsail as the main control interface
- OrcaSlicer as the recommended slicer

---

## Main Printer Components

The main parts of the My-Cloner are:

- Frame
- X-axis
- Y-axis
- Dual-motor Z-axis
- Direct-drive extruder
- V6-style hotend
- Heated bed
- Smooth PEI spring steel sheet
- P.I.N.D.A. probe
- Filament sensor
- MKS Robin Nano V3.0 mainboard
- Raspberry Pi Zero 2 W
- MKS TS35 V2.0 display
- Mean Well LRS-350-24 power supply

<figure markdown="1">
  ![My-Cloner Printer Overview](/assets/images/image-placeholder.webp#only-light){ width="700" }
  ![My-Cloner Printer Overview](/assets/images/image-placeholder.webp#only-dark){ width="700" }
  <figcaption>Main components of the My-Cloner Rev A.</figcaption>
</figure>

---

## Axis Movement

| Axis | Movement |
|---|---|
| **X** | Extruder moves left and right |
| **Y** | Print bed moves forwards and backwards |
| **Z** | X-axis gantry moves up and down |
| **E** | Extruder feeds or retracts filament |

Understanding these directions is important before performing the first homing procedure.

---

## Key Specifications

| Feature | Specification |
|---|---|
| **Hardware Revision** | Rev A |
| **Build Volume** | TBD — actual travel and printable area pending measurement |
| **Filament Diameter** | 1.75 mm |
| **Standard Nozzle** | 0.4 mm |
| **Intended Hotend Temperature Target** | 300 °C — Pending validation; operating limit TBD |
| **Heatbed Size** | 235 × 235 mm; Ender 3 type, 24 V, 220 W |
| **Electrical System** | 24 V DC |
| **Firmware** | Klipper |
| **Main Interface** | Mainsail |
| **Recommended Slicer** | OrcaSlicer |

---

## Control Architecture

The My-Cloner uses Klipper's host-and-MCU architecture.

The **Raspberry Pi Zero 2 W** runs the Klipper host software and Mainsail.

The **MKS Robin Nano V3** acts as the printer MCU and controls the motors, heaters, fans, sensors and probe.

---

## Current Machine Status

The printer is assembled and has undergone earlier tests. A clean Klipper/Mainsail installation is planned; the earlier configuration is unavailable. The estimated extra 10 mm travel beyond each bed edge is provisional and must not be used as validated motion limits. See the [hardware and test record](../../wiring/io-map.md#owner-reported-hardware-and-test-status).

## Next Steps

Before powering on the printer for the first time, complete the pre-power checks:

[Before First Power-On](before-first-power-on.md)

After the checks are complete:

[First Power-On](first-power-on.md)

Then continue with:

[First Time Setup & Calibration](first-time-setup.md)