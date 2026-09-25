# My-Cloner Rev A — I/O Map

This page defines the electrical I/O mapping used by the **My-Cloner Rev A**.

The purpose of this document is to provide a single reference between:

- Physical printer hardware
- MKS Robin Nano V3 connectors
- STM32F407 MCU pins
- TMC2209 stepper drivers
- Klipper configuration
- Electrical schematic
- Hardware validation status

!!! warning "Engineering Reference"
    This document contains both board-level pin mappings confirmed by the official Makerbase and Klipper sources and My-Cloner-specific assignments.

    My-Cloner-specific assignments must be physically validated before the machine is considered ready for operation.

## Official References

The board-level mappings in this document are based on the official project sources:

- [MKS Robin Nano V3.X — Makerbase GitHub](https://github.com/makerbase-mks/MKS-Robin-Nano-V3.X){ target="_blank" rel="noopener noreferrer" }
- [Klipper — Generic MKS Robin Nano V3 Configuration](https://github.com/Klipper3d/klipper/blob/master/config/generic-mks-robin-nano-v3.cfg){ target="_blank" rel="noopener noreferrer" }
- [Klipper — TMC Driver Documentation](https://github.com/Klipper3d/klipper/blob/master/docs/TMC_Drivers.md){ target="_blank" rel="noopener noreferrer" }

The official Makerbase schematic identifies the controller as the **MKS Robin Nano V3**, based on the **STM32F407VGT6** MCU.

---

## Controller Overview

| Item | My-Cloner Rev A |
|---|---|
| Mainboard | MKS Robin Nano V3 |
| MCU | STM32F407VGT6 |
| Main supply | 24 V DC |
| Firmware | Klipper |
| Host | Raspberry Pi Zero 2 W |
| Stepper drivers | 5 × TMC2209 |
| Driver communication | UART |
| X/Y homing | TMC2209 sensorless homing |
| Z reference | P.I.N.D.A. probe |
| Primary user interface | Mainsail |
| Local display | MKS TS35 V2.0 — integration under validation |

---

## Stepper Driver Mapping

The MKS Robin Nano V3 provides five stepper-driver positions:

- X
- Y
- Z
- E0
- E1

The My-Cloner Rev A uses all five driver positions.

| Board Driver | My-Cloner Function | Driver | Communication | Status |
|---|---|---|---|---|
| X | X Axis | TMC2209 | UART | Planned |
| Y | Y Axis | TMC2209 | UART | Planned |
| Z | Left Z Axis | TMC2209 | UART | Planned |
| E0 | Extruder | TMC2209 | UART | Planned |
| E1 | Right Z Axis | TMC2209 | UART | Planned |

!!! note "Z Motor Assignment"
    The current Rev A assignment uses the board's **Z driver for the Left Z motor** and the **E1 driver for the Right Z motor**.

    This assignment must be confirmed during the physical wiring and Klipper bring-up process.

### Step / Direction / Enable Pins

| Function | Board Driver | STEP | DIR | ENABLE | Klipper Section | Status |
|---|---|---:|---:|---:|---|---|
| X Axis | X | `PE3` | `PE2` | `PE4` | `[stepper_x]` | Source confirmed |
| Y Axis | Y | `PE0` | `PB9` | `PE1` | `[stepper_y]` | Source confirmed |
| Left Z Axis | Z | `PB5` | `PB4` | `PB8` | `[stepper_z]` | Source confirmed |
| Extruder | E0 | `PD6` | `PD3` | `PB3` | `[extruder]` | Source confirmed |
| Right Z Axis | E1 | `PD15` | `PA1` | `PA3` | `[stepper_z1]` | Source confirmed / Rev A assignment |

The final Klipper configuration may invert individual direction or enable pins using the `!` prefix.

The required polarity will be confirmed during motor-direction testing.

---

## TMC2209 UART Mapping

The official MKS Robin Nano V3 pin map provides a dedicated UART line for each stepper-driver position.

| Board Driver | UART Pin | My-Cloner Function | Status |
|---|---:|---|---|
| X | `PD5` | X Axis | Source confirmed |
| Y | `PD7` | Y Axis | Source confirmed |
| Z | `PD4` | Left Z Axis | Source confirmed |
| E0 | `PD9` | Extruder | Source confirmed |
| E1 | `PD8` | Right Z Axis | Source confirmed |

These pins will be used by the Klipper `[tmc2209 ...]` sections.

Example structure:

    [tmc2209 stepper_x]
    uart_pin: PD5

    [tmc2209 stepper_y]
    uart_pin: PD7

    [tmc2209 stepper_z]
    uart_pin: PD4

    [tmc2209 extruder]
    uart_pin: PD9

    [tmc2209 stepper_z1]
    uart_pin: PD8

!!! warning "Do Not Copy Driver Settings Yet"
    UART pin assignments are board-level information.

    Driver current, `run_current`, `hold_current`, interpolation and StallGuard settings must be defined and validated separately for the actual My-Cloner motors.

---

## Sensorless Homing

The My-Cloner Rev A is planned to use **TMC2209 sensorless homing on the X and Y axes**.

The Robin Nano V3 exposes the driver DIAG signals as follows:

| Driver DIAG | Board Endstop Input | MCU Pin | My-Cloner Use | Status |
|---|---|---:|---|---|
| X DIAG | X- | `PA15` | X sensorless homing | Planned |
| Y DIAG | Y- | `PD2` | Y sensorless homing | Planned |
| Z DIAG | Z- | `PC8` | Not used for normal Z homing | Available |
| E0 DIAG | Z+ | `PC4` | Not currently used | Available |
| E1 DIAG | E1- | `PE7` | Not currently used | Available |

The official Makerbase circuit maps the DIAG signals to the corresponding endstop inputs.

!!! warning "Sensorless Homing Requires Physical Tuning"
    Sensorless homing cannot be considered validated from configuration alone.

    The following must be tested on the physical printer:

    - Driver current
    - StallGuard threshold
    - Homing speed
    - Mechanical friction
    - Belt tension
    - Homing direction
    - Repeatability

The final StallGuard values will therefore be added only after physical machine testing.

---

## Z Probe

The My-Cloner Rev A uses a **P.I.N.D.A. inductive probe** for Z referencing and bed probing.

| Function | Device | Board Input | MCU Pin | Status |
|---|---|---|---:|---|
| Z Probe | P.I.N.D.A. | Z probe / endstop input | TBD | Pending wiring validation |

The Robin Nano V3 provides several possible probe-related inputs, including the Z endstop input and a dedicated BLTouch interface.

The final P.I.N.D.A. connection must match the My-Cloner electrical schematic.

!!! important "Do Not Assume BLTouch Wiring"
    The My-Cloner uses a P.I.N.D.A. probe, not a BLTouch.

    The dedicated Robin Nano V3 BLTouch control pin (`PA8`) must not automatically be assumed to be the correct P.I.N.D.A. signal input.

    The final connection will be documented after the probe wiring is confirmed.

---

## Extruder

| Function | Device | Board Driver / Output | MCU Pin | Status |
|---|---|---|---:|---|
| Extruder Motor | NEMA17 Pancake | E0 | STEP `PD6` | Source confirmed |
| Extruder Direction | — | E0 | DIR `PD3` | Source confirmed |
| Extruder Enable | — | E0 | EN `PB3` | Source confirmed |
| Extruder Driver UART | TMC2209 | E0 | `PD9` | Source confirmed |

The E0 driver is reserved for the direct-drive extruder.

---

## Hotend

### Heater

| Function | Board Output | MCU Pin | Voltage | Status |
|---|---|---:|---|---|
| Hotend Heater | HE0 | `PE5` | 24 V DC | Source confirmed |

The generic Klipper configuration uses:

    heater_pin: PE5

The My-Cloner Rev A uses a 24 V V6-style heater cartridge.

The exact heater power must still be documented in the final hardware specification.

### Thermistor

| Function | Board Input | MCU Pin | Status |
|---|---|---:|---|
| Hotend Thermistor | TH1 | `PC1` | Source confirmed |

The generic Klipper configuration uses `PC1` for the hotend thermistor input.

!!! warning "Thermistor Type Pending"
    The electrical input pin is confirmed.

    The exact My-Cloner Rev A hotend thermistor model and corresponding Klipper `sensor_type` still require final confirmation.

    Do not copy the generic Klipper thermistor type without validating the installed sensor.

---

## Heated Bed

### Heater

| Function | Board Output | MCU Pin | Voltage | Status |
|---|---|---:|---|---|
| Heated Bed | H-BED | `PA0` | 24 V DC | Source confirmed |

The generic Klipper configuration uses:

    heater_pin: PA0

### Thermistor

| Function | Board Input | MCU Pin | Status |
|---|---|---:|---|
| Heated Bed Thermistor | TB | `PC0` | Source confirmed |

The generic Klipper configuration uses:

    sensor_pin: PC0

The generic Klipper example specifies an EPCOS 100K thermistor.

The exact thermistor fitted to the My-Cloner Rev A heated bed must still be confirmed before the final Klipper configuration is released.

---

## Cooling Fans

The Robin Nano V3 provides two controllable fan outputs.

| Function | Board Output | MCU Pin | My-Cloner Device | Status |
|---|---|---:|---|---|
| Fan 1 | FAN1 | `PC14` | TBD | Source confirmed / Assignment pending |
| Fan 2 | FAN2 | `PB1` | TBD | Source confirmed / Assignment pending |

The My-Cloner uses:

- 1 × 4010 24 V hotend cooling fan
- 1 × 5015 24 V part-cooling blower

The final assignment between FAN1/FAN2 and the two physical fans will be confirmed from the electrical schematic and physical wiring.

!!! note "Klipper Generic Configuration"
    The generic Robin Nano V3 Klipper example uses `PC14` as the primary `[fan]` output and lists `PB1` as the second available fan output.

    The My-Cloner configuration does not need to follow that functional assignment if the wiring requires a different mapping.

---

## Filament Sensor

The My-Cloner Rev A uses an **MK3-style IR filament sensor** with the mechanical ball and magnet mechanism.

The Robin Nano V3 provides two material-detection inputs:

| Board Input | MCU Pin | My-Cloner Use | Status |
|---|---:|---|---|
| MT_DET1 | `PA4` | Candidate filament sensor input | Pending validation |
| MT_DET2 | `PE6` | Available | Pending validation |

The final input will be selected according to the electrical schematic.

---

## Display

The My-Cloner Rev A hardware includes an **MKS TS35 V2.0** display.

Its final Klipper integration is still under investigation.

### EXP1 Header

| Pin | MCU / Function |
|---|---|
| EXP1_1 | `PC5` |
| EXP1_2 | `PE13` |
| EXP1_3 | `PD13` |
| EXP1_4 | `PC6` |
| EXP1_5 | `PE14` |
| EXP1_6 | `PE15` |
| EXP1_7 | `PD11` |
| EXP1_8 | `PD10` |
| EXP1_9 | GND |
| EXP1_10 | 5 V |

### EXP2 Header

| Pin | MCU / Function |
|---|---|
| EXP2_1 | `PA6` |
| EXP2_2 | `PA5` |
| EXP2_3 | `PE8` |
| EXP2_4 | `PE10` |
| EXP2_5 | `PE11` |
| EXP2_6 | `PA7` |
| EXP2_7 | `PE12` |
| EXP2_8 | RESET |
| EXP2_9 | GND |
| EXP2_10 | 3.3 V |

!!! warning "Display Integration Not Final"
    These are the Robin Nano V3 EXP-header pin mappings.

    They do not by themselves confirm that the MKS TS35 V2.0 will operate directly through Klipper.

    **Mainsail remains the primary My-Cloner Rev A user interface.**

---

## Raspberry Pi and MCU Communication

The Raspberry Pi Zero 2 W will run Klipper and Mainsail.

The MKS Robin Nano V3 generic Klipper configuration is intended for:

- MCU: STM32F407
- Bootloader: 48 KiB
- Communication: USB

The official generic configuration instructs users to compile Klipper for the STM32F407 and use USB communication.

The Raspberry Pi is powered separately through the My-Cloner 24 V → 5 V LM2596 supply.

---

## Power Control and Auxiliary Inputs

The Robin Nano V3 also exposes the following auxiliary signals:

| Function | MCU Pin | My-Cloner Rev A |
|---|---:|---|
| Power Detect | `PA13` | Not currently implemented |
| Power Off | `PB2` | Not currently implemented |
| Material Detect 1 | `PA4` | Candidate filament sensor |
| Material Detect 2 | `PE6` | Available |
| BLTouch Control | `PA8` | Not currently assigned |

Power Panic / power-loss recovery is **not implemented in the current My-Cloner Rev A**.

These signals remain available for future development.

---

## My-Cloner Rev A Summary

| Function | Board Connection | MCU Pin | Klipper Section | Status |
|---|---|---:|---|---|
| X Motor STEP | X | `PE3` | `[stepper_x]` | Source confirmed |
| X Motor DIR | X | `PE2` | `[stepper_x]` | Source confirmed |
| X Motor EN | X | `PE4` | `[stepper_x]` | Source confirmed |
| X TMC UART | X | `PD5` | `[tmc2209 stepper_x]` | Source confirmed |
| X Sensorless | X- | `PA15` | `[stepper_x]` | Planned |
| Y Motor STEP | Y | `PE0` | `[stepper_y]` | Source confirmed |
| Y Motor DIR | Y | `PB9` | `[stepper_y]` | Source confirmed |
| Y Motor EN | Y | `PE1` | `[stepper_y]` | Source confirmed |
| Y TMC UART | Y | `PD7` | `[tmc2209 stepper_y]` | Source confirmed |
| Y Sensorless | Y- | `PD2` | `[stepper_y]` | Planned |
| Left Z STEP | Z | `PB5` | `[stepper_z]` | Source confirmed |
| Left Z DIR | Z | `PB4` | `[stepper_z]` | Source confirmed |
| Left Z EN | Z | `PB8` | `[stepper_z]` | Source confirmed |
| Left Z UART | Z | `PD4` | `[tmc2209 stepper_z]` | Source confirmed |
| Right Z STEP | E1 | `PD15` | `[stepper_z1]` | Rev A assignment |
| Right Z DIR | E1 | `PA1` | `[stepper_z1]` | Rev A assignment |
| Right Z EN | E1 | `PA3` | `[stepper_z1]` | Rev A assignment |
| Right Z UART | E1 | `PD8` | `[tmc2209 stepper_z1]` | Rev A assignment |
| Extruder STEP | E0 | `PD6` | `[extruder]` | Source confirmed |
| Extruder DIR | E0 | `PD3` | `[extruder]` | Source confirmed |
| Extruder EN | E0 | `PB3` | `[extruder]` | Source confirmed |
| Extruder UART | E0 | `PD9` | `[tmc2209 extruder]` | Source confirmed |
| Hotend Heater | HE0 | `PE5` | `[extruder]` | Source confirmed |
| Hotend Thermistor | TH1 | `PC1` | `[extruder]` | Source confirmed |
| Heated Bed | H-BED | `PA0` | `[heater_bed]` | Source confirmed |
| Bed Thermistor | TB | `PC0` | `[heater_bed]` | Source confirmed |
| Fan 1 | FAN1 | `PC14` | TBD | Function pending |
| Fan 2 | FAN2 | `PB1` | TBD | Function pending |
| P.I.N.D.A. | TBD | TBD | `[probe]` | Wiring pending |
| Filament Sensor | MT_DET1 / TBD | `PA4` / TBD | `[filament_switch_sensor]` | Pending validation |
| Display | EXP / TBD | TBD | TBD | Under validation |

---

## Status Definitions

| Status | Meaning |
|---|---|
| **Source confirmed** | Mapping is confirmed by the official board/Klipper source |
| **Rev A assignment** | My-Cloner-specific design decision based on the available board resources |
| **Planned** | Intended configuration but not physically validated |
| **Pending validation** | Requires schematic or physical-machine confirmation |
| **Validated** | Tested successfully on the physical My-Cloner Rev A |

---

## Validation Procedure

Each My-Cloner I/O point should pass through the following process:

1. Confirm the board-level pin from the official Makerbase documentation.
2. Confirm the Klipper MCU pin mapping.
3. Confirm the My-Cloner QElectroTech wiring.
4. Verify connector orientation and supply voltage.
5. Add the corresponding configuration to `printer.cfg`.
6. Test the function safely on the physical machine.
7. Record the result.
8. Change the status to **Validated** only after successful testing.

!!! danger "Never Validate by Assumption"
    A correct MCU pin does not guarantee that a connected device is wired correctly.

    Voltage, polarity, connector orientation and device specifications must always be verified before power is applied.

---

## Related Documentation

- [System Overview](system-overview.md)
- [Power Distribution](power-distribution.md)
- [Controller Board](controller-board.md)
- [Motors & Homing](motors-and-homing.md)
- [Heaters & Temperature Sensors](heaters-and-temperature-sensors.md)
- [Fans](fans.md)
- [Display & Filament Sensor](display-and-filament-sensor.md)
- [Firmware Configuration](../downloads/firmware-configuration.md)