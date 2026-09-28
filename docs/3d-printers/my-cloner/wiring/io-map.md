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

!!! info "Engineering Reference"
    This document contains both board-level pin mappings confirmed by the official Makerbase and Klipper sources and My-Cloner-specific assignments.

    My-Cloner-specific assignments must be physically validated before the machine is considered ready for operation.

## Official References

The board-level mappings in this document are based on the official project sources:

- [MKS Robin Nano V3.X — Makerbase GitHub](https://github.com/makerbase-mks/MKS-Robin-Nano-V3.X){ target="_blank" rel="noopener noreferrer" }
- [Klipper — Generic MKS Robin Nano V3 Configuration](https://github.com/Klipper3d/klipper/blob/master/config/generic-mks-robin-nano-v3.cfg){ target="_blank" rel="noopener noreferrer" }
- [Klipper — TMC Driver Documentation](https://github.com/Klipper3d/klipper/blob/master/docs/TMC_Drivers.md){ target="_blank" rel="noopener noreferrer" }

The official Makerbase schematic identifies the controller as the **MKS Robin Nano V3**, based on the **STM32F407VGT6** MCU.

---

## Owner-Reported Hardware and Test Status

The owner confirmed these details on 2026-09-28. They describe the assembled My-Cloner Rev A; they are not a complete commissioning record.

| Item | Confirmed hardware / connection | Status |
|---|---|---|
| Controller | MKS Robin Nano V3.0 | Rev A assignment |
| Host | Raspberry Pi Zero 2 W; microSD and reader available; clean Klipper/Mainsail installation required | Rev A assignment |
| X / Y / left Z / right Z motors | 17HS13-0404S1; manufacturer rating 0.4 A per phase | Rev A assignment |
| Extruder motor | 17HS10-0704S; manufacturer rating 0.7 A per phase; direct gear drive without reduction | Rev A assignment |
| X/Y transmission | GT2 20-tooth pulleys, as listed in the mechanical BOM | Rev A assignment |
| Z transmission | 2 mm pitch; 8 mm lead per revolution | Rev A assignment |
| X/Y homing | TMC2209 sensorless homing selected; DIAG jumpers reported installed | Rev A assignment |
| P.I.N.D.A. | V1, three wires; Z- / PC8, GND and 5 V as reported by owner | Rev A assignment |
| Hotend fan | 4010, 24 V; FAN1 / PC14 | Rev A assignment |
| Part-cooling fan | 5015, 24 V; FAN2 / PB1 | Rev A assignment |
| Filament sensor | IR V0.4; MT_DET1 / PA4 | Rev A assignment |
| Hotend heater | 24 V, 40 W; cartridge Ø6 × 21 mm | Rev A assignment |
| Hotend thermistor | Owner-identified ATC Semitec 104GT-2, NTC 100 kΩ; reported cartridge Ø3 × 15 mm | Rev A assignment |
| Heated bed | Ender 3 type, 24 V, 220 W, 235 × 235 mm | Rev A assignment |
| Bed thermistor | Original bed NTC 100 kΩ; exact curve / Klipper sensor_type still TBD | Pending validation |

The owner reports checking the hotend heater resistance against the expected 12–15 Ω range and the hotend thermistor against approximately 100 kΩ at 25 °C. Exact readings and measurement conditions were not recorded here. The P.I.N.D.A. responds to nearby metal; its Klipper open/triggered polarity and Z offset still require verification.

Earlier Klipper tests were performed and errors were resolved, but calibration was unfinished and no printer.cfg or log survives. A clean installation and a new configuration are planned. Recheck each subsystem with that configuration before marking it Validated.

The owner's provisional X/Y travel estimate is 10 mm beyond each edge of the 235 mm bed (255 mm total span per axis). This is not a measured printable area or approved position_min/position_max. Coordinate origin, X/Y limits, Z travel and probe offsets remain pending measurement.

### Motor Sources

- [STEPPERONLINE 17HS13-0404S1](https://www.omc-stepperonline.com/download/17HS13-0404S1.pdf): 0.4 A per phase. The earlier 0.7 A entry for this model is superseded.
- [STEPPERONLINE 17HS10-0704S](https://www.omc-stepperonline.com/fr/nema-17-bipolaire-1-8deg-13ncm-18-4oz-in-0-7a-2-9v-42x42x25mm-4-fils-17hs10-0704s): 0.7 A per phase.

Motor nameplate current is not an automatically validated Klipper run_current. Driver settings remain to be selected and tested.

## Controller Overview

| Item | My-Cloner Rev A |
|---|---|
| Controller board | MKS Robin Nano V3.0 |
| MCU | STM32F407VGT6 |
| Main supply | 24 V DC |
| Firmware | Klipper |
| Host | Raspberry Pi Zero 2 W |
| Stepper drivers | 5 × TMC2209 |
| Driver communication | UART |
| X/Y homing | TMC2209 sensorless homing |
| Z reference | P.I.N.D.A. probe |
| Primary user interface | Mainsail |
| Local display | MKS TS35 V2.0 — integration: Pending validation |

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
| X | X Axis | TMC2209 | UART | Rev A assignment |
| Y | Y Axis | TMC2209 | UART | Rev A assignment |
| Z | Left Z Axis | TMC2209 | UART | Rev A assignment |
| E0 | Extruder | TMC2209 | UART | Rev A assignment |
| E1 | Right Z Axis | TMC2209 | UART | Rev A assignment |

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

```ini
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
```

!!! warning "Do Not Copy Driver Settings Yet"
    UART pin assignments are board-level information.

    Driver current, `run_current`, `hold_current`, interpolation and StallGuard settings must be defined and validated separately for the actual My-Cloner motors.

---

## Sensorless Homing

The My-Cloner Rev A uses **TMC2209 sensorless homing on the X and Y axes**.

This is a Rev A design assignment. The final driver current, StallGuard threshold, homing speed and homing repeatability remain pending physical validation.

The MKS Robin Nano V3 exposes the driver DIAG signals as follows:

| Driver DIAG | Board Endstop Input | MCU Pin | My-Cloner Use | Status |
|---|---|---:|---|---|
| X DIAG | X- | `PA15` | X sensorless homing | Rev A assignment |
| Y DIAG | Y- | `PD2` | Y sensorless homing | Rev A assignment |
| Z DIAG / Z- | Z- | `PC8` | Assigned to P.I.N.D.A. V1; Z sensorless homing not used | Rev A assignment |
| E0 DIAG | Z+ | `PC4` | Not currently used | Source confirmed |
| E1 DIAG | E1- | `PE7` | Not currently used | Source confirmed |

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
| Z Probe | P.I.N.D.A. V1, three wires | Z- | `PC8` | Rev A assignment |

The MKS Robin Nano V3 provides several possible probe-related inputs, including the Z endstop input and a dedicated BLTouch interface.

The owner reports Z- / PC8, GND and 5 V connections. Response to metal has been observed; Klipper trigger polarity, electrical interface and offsets remain pending validation.

!!! important "Do Not Assume BLTouch Wiring"
    The My-Cloner uses a P.I.N.D.A. probe, not a BLTouch.

    The dedicated MKS Robin Nano V3 BLTouch control pin (`PA8`) must not automatically be assumed to be the correct P.I.N.D.A. signal input.

    PC8 is the reported Rev A signal input. Confirm the electrical interface and open/triggered readings before Z homing.

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

```ini
heater_pin: PE5
```

The My-Cloner Rev A uses a 24 V V6-style heater cartridge.

The owner identifies the cartridge as 24 V, 40 W, Ø6 × 21 mm and reports checking its resistance against the expected 12–15 Ω range.

### Thermistor

| Function | Board Input | MCU Pin | Status |
|---|---|---:|---|
| Hotend Thermistor | TH1 | `PC1` | Source confirmed |

The generic Klipper configuration uses `PC1` for the hotend thermistor input.

!!! warning "Temperature Validation Pending"
    The electrical input pin is confirmed.

    The owner identifies the installed hotend thermistor as ATC Semitec 104GT-2. Temperature readings and thermal limits must be verified with the new configuration.

    Do not copy the generic Klipper thermistor type without validating the installed sensor.

---

## Heated Bed

### Heater

| Function | Board Output | MCU Pin | Voltage | Status |
|---|---|---:|---|---|
| Heated Bed | H-BED | `PA0` | 24 V DC | Source confirmed |

The generic Klipper configuration uses:

```ini
heater_pin: PA0
```

### Thermistor

| Function | Board Input | MCU Pin | Status |
|---|---|---:|---|
| Heated Bed Thermistor | TB | `PC0` | Source confirmed |

The generic Klipper configuration uses:

```ini
sensor_pin: PC0
```

The generic Klipper example specifies an EPCOS 100K thermistor.

The installed Ender 3 bed is 24 V, 220 W and 235 × 235 mm, with its original NTC 100 kΩ thermistor. Its exact curve / sensor_type remains TBD; the generic EPCOS example is not confirmation of the fitted sensor.

---

## Cooling Fans

The MKS Robin Nano V3 provides two controllable fan outputs.

| Function | Board Output | MCU Pin | My-Cloner Device | Status |
|---|---|---:|---|---|
| Hotend fan | FAN1 | `PC14` | 4010, 24 V | Rev A assignment |
| Part-cooling fan | FAN2 | `PB1` | 5015, 24 V | Rev A assignment |

The My-Cloner uses:

- 1 × 4010 24 V hotend cooling fan
- 1 × 5015 24 V part-cooling blower

The owner reports these fan connections on the assembled printer. PWM, airflow and control under the new configuration remain pending validation.

!!! note "Klipper Generic Configuration"
    The generic MKS Robin Nano V3 Klipper example uses `PC14` as the primary `[fan]` output and lists `PB1` as the second available fan output.

    The My-Cloner configuration does not need to follow that functional assignment if the wiring requires a different mapping.

---

## Filament Sensor

The My-Cloner Rev A uses an **MK3-style IR filament sensor** with the mechanical ball and magnet mechanism.

The MKS Robin Nano V3 provides two material-detection inputs:

| Board Input | MCU Pin | My-Cloner Use | Status |
|---|---:|---|---|
| MT_DET1 | `PA4` | IR V0.4 filament sensor | Rev A assignment |
| MT_DET2 | `PE6` | Available / not assigned | Source confirmed |

MT_DET1 / PA4 is the owner-reported connection; sensor supply, signal polarity and runout behaviour remain pending validation.

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

!!! warning "Display Integration Pending Validation"
    These are the MKS Robin Nano V3 EXP-header pin mappings.

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

The MKS Robin Nano V3 also exposes the following auxiliary signals:

| Function | MCU Pin | My-Cloner Rev A |
|---|---:|---|
| Power Detect | `PA13` | Not currently implemented |
| Power Off | `PB2` | Not currently implemented |
| MT_DET1 | `PA4` | IR V0.4 filament sensor |
| MT_DET2 | `PE6` | Available |
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
| X Sensorless | X- | `PA15` | `[stepper_x]` | Rev A assignment |
| Y Motor STEP | Y | `PE0` | `[stepper_y]` | Source confirmed |
| Y Motor DIR | Y | `PB9` | `[stepper_y]` | Source confirmed |
| Y Motor EN | Y | `PE1` | `[stepper_y]` | Source confirmed |
| Y TMC UART | Y | `PD7` | `[tmc2209 stepper_y]` | Source confirmed |
| Y Sensorless | Y- | `PD2` | `[stepper_y]` | Rev A assignment |
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
| Hotend fan 4010 | FAN1 | `PC14` | `[heater_fan hotend_fan]` planned | Rev A assignment |
| Part-cooling fan 5015 | FAN2 | `PB1` | `[fan]` planned | Rev A assignment |
| P.I.N.D.A. V1 | Z- | `PC8` | `[probe]` | Rev A assignment |
| IR V0.4 Filament Sensor | MT_DET1 | `PA4` | `[filament_switch_sensor]` | Rev A assignment |
| Display | EXP / TBD | TBD | TBD | Pending validation |

---

## Status Definitions

`Source confirmed` applies only to the board mapping. `Rev A assignment` records a design choice; neither status confirms hardware operation. Combined entries describe these separate aspects. No physical test result is established by this page.

`MT_DET` denotes the material-detection input family; use `MT_DET1` or `MT_DET2` for an identified connector. The owner reports the IR V0.4 sensor connected to MT_DET1 / PA4; supply, polarity and runout behaviour still require verification.

| Status | Meaning |
|---|---|
| **Source confirmed** | Mapping is confirmed by the official board/Klipper source |
| **Rev A assignment** | My-Cloner-specific design decision based on the available board resources |
| **Planned** | Intended configuration but not physically validated |
| **Pending validation** | Requires schematic or physical-machine confirmation |
| **TBD** | Value or assignment has not yet been determined |
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

!!! warning "Never Validate by Assumption"
    A correct MCU pin does not guarantee that a connected device is wired correctly.

    Voltage, polarity, connector orientation and device specifications must always be verified before power is applied.

---

## Related Documentation

- [System Overview](system-overview.md) — complete Rev A electrical architecture
- [Power Distribution](power-distribution.md) — AC, 24 V and 5 V power architecture
- [Controller Board](controller-board.md) — MKS Robin Nano V3 hardware interfaces
- [Motors & Homing](motors-and-homing.md) — stepper drivers, motors and homing
- [Heaters & Temperature Sensors](heaters-and-temperature-sensors.md) — heater and thermistor wiring
- [Fans](fans.md) — cooling hardware and fan outputs
- [Display & Filament Sensor](display-and-filament-sensor.md) — TS35 and filament-sensor integration
- [Firmware Configuration](../downloads/firmware-configuration.md) — planned Klipper configuration