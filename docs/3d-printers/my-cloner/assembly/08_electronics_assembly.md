# Electronics Assembly

This chapter covers the installation and connection of the **My-Cloner Rev A electronics**.

The Rev A electrical architecture uses:

- MKS Robin Nano V3
- 5 × TMC2209 stepper drivers in UART mode
- Raspberry Pi Zero 2 W
- LM2596 24 V → 5 V converter
- P.I.N.D.A. probe
- MK3-style IR filament sensor
- MKS TS35 V2.0 display
- 24 V hotend, heated bed and cooling fans

!!! warning "Rev A Validation Status"
    The board-level pin mapping is documented, but several My-Cloner-specific connections still require physical validation.

    Do not infer a connection from older MK3S/Einsy assembly instructions.

    Use the current [I/O Map](../wiring/io-map.md) and the approved QElectroTech schematic as the electrical reference.

---

## Before You Start

Disconnect the printer from mains power before installing or modifying electronics.

Confirm that you have reviewed:

- [Power Distribution](../wiring/power-distribution.md)
- [Controller Board](../wiring/controller-board.md)
- [I/O Map](../wiring/io-map.md)
- [Motors & Homing](../wiring/motors-and-homing.md)
- [Heaters & Temperature Sensors](../wiring/heaters-and-temperature-sensors.md)
- [Fans](../wiring/fans.md)
- [Display & Filament Sensor](../wiring/display-and-filament-sensor.md)

!!! danger "Mains Voltage"
    The printer contains 230 V AC wiring.

    Do not work on the mains side while the printer is connected to the power outlet.

---

## 1. Prepare the Electronics Housing

Use the current My-Cloner Rev A printed parts from the BOM:

- Makerbase Board Housing
- Makerbase Housing Lid
- Makerbase Cable Clip
- PSU Cover where applicable

Inspect the printed parts for cracks, warping or damaged mounting features before installation.

Do not use inherited electronics housings unless their compatibility with the Robin Nano V3 and Rev A cable routing has been explicitly confirmed.

---

## 2. Install the MKS Robin Nano V3

Mount the **MKS Robin Nano V3** in the electronics housing using the mounting features defined by the current My-Cloner mechanical design.

Before tightening the board:

1. Confirm that the PCB is not under mechanical stress.
2. Ensure that no screw head or metallic part can short exposed PCB contacts.
3. Leave access to the stepper-driver sockets, power terminals, USB connector and required I/O connectors.
4. Confirm that the housing allows safe cable routing and strain relief.

Handle the board by its edges and observe normal ESD precautions.

---

## 3. Install the TMC2209 Drivers

The My-Cloner Rev A uses **5 × TMC2209** drivers.

| Robin Nano Position | Rev A Function |
|---|---|
| X | X axis |
| Y | Y axis |
| Z | Left Z axis |
| E0 | Extruder |
| E1 | Right Z axis |

The drivers are intended to operate in **UART mode**.

!!! warning "Driver Orientation"
    Verify the physical orientation and jumper configuration against the Robin Nano V3 and TMC2209 documentation before applying power.

    Incorrect driver orientation can damage the driver or controller.

Final motor currents and StallGuard parameters are established during physical bring-up, not during mechanical assembly.

---

## 4. Install the Raspberry Pi Power Branch

The Raspberry Pi Zero 2 W is **not powered from the Robin Nano V3 as the primary Rev A supply method**.

The Rev A architecture is:

```mermaid
graph LR
    PSU[24 V DC] --> LM[LM2596]
    LM -->|5 V DC| PI[Raspberry Pi Zero 2 W]
    PI -->|USB| BOARD[MKS Robin Nano V3]
```

Before connecting the Raspberry Pi:

1. Power and adjust the LM2596 without the Pi connected.
2. Measure the output with a multimeter.
3. Confirm approximately **5 V DC** with correct polarity.
4. Switch off power.
5. Only then connect the Raspberry Pi.

See [Power Distribution](../wiring/power-distribution.md) for the full architecture.

---

## 5. Connect the Stepper Motors

Connect the motors according to the Rev A driver assignment:

| Motor | Driver Position |
|---|---|
| X | X |
| Y | Y |
| Left Z | Z |
| Right Z | E1 |
| Extruder | E0 |

Do not perform homing during this stage.

Motor direction, current and dual-Z behaviour must be validated individually during bring-up.

---

## 6. Connect the Hotend and Heated Bed

The source-confirmed controller channels are:

| Function | Board Channel | MCU Pin |
|---|---|---:|
| Hotend heater | HE0 | `PE5` |
| Heated bed | H-BED | `PA0` |
| Hotend thermistor | TH1 | `PC1` |
| Bed thermistor | TB | `PC0` |

!!! important "Thermistor Models Pending"
    The controller pins are known, but the exact installed thermistor models still require confirmation.

    Do not finalize Klipper `sensor_type` values until the physical sensors are identified.

The exact heater powers also remain pending confirmation.

---

## 7. Connect the Cooling Fans

The Robin Nano V3 exposes:

| Output | MCU Pin |
|---|---:|
| FAN1 | `PC14` |
| FAN2 | `PB1` |

The My-Cloner Rev A uses:

- 4010 24 V hotend cooling fan
- 5015 24 V part-cooling blower

The functional FAN1/FAN2 assignment is still pending validation.

Do not assume a fan assignment from an older printer. The physical wiring and final Klipper configuration must agree.

---

## 8. Connect the P.I.N.D.A. Probe

The My-Cloner Rev A uses a **P.I.N.D.A. probe**, not a SuperPINDA or BLTouch.

The final Robin Nano input for the P.I.N.D.A. is still pending confirmation against the Rev A electrical schematic and physical machine.

!!! warning "Do Not Guess the Probe Input"
    The presence of Z-endstop and BLTouch-related board inputs does not identify the correct P.I.N.D.A. connection automatically.

    Follow the validated Rev A I/O assignment before connecting the probe.

---

## 9. Connect the IR Filament Sensor

The Robin Nano V3 exposes two material-detection inputs:

| Input | MCU Pin |
|---|---:|
| MT_DET1 | `PA4` |
| MT_DET2 | `PE6` |

The final My-Cloner Rev A filament-sensor input and signal polarity remain pending validation.

Before connecting the sensor, confirm:

- Supply voltage
- Ground
- Signal pin
- Connector orientation
- Active-high / active-low behaviour

---

## 10. Connect the MKS TS35 V2.0

The MKS TS35 V2.0 is part of the Rev A hardware, but its final Klipper integration is still under validation.

**Mainsail remains the primary user interface.**

Do not connect the display solely by copying EXP1/EXP2 ribbon-cable instructions from another printer.

Use the current [Display & Filament Sensor](../wiring/display-and-filament-sensor.md) documentation once the TS35 interface has been validated.

---

## 11. Connect the Raspberry Pi to the Controller

Klipper host communication uses **USB** between:

- Raspberry Pi Zero 2 W
- MKS Robin Nano V3

Route the USB cable so that it:

- Cannot enter the motion envelope
- Is not sharply bent
- Does not place stress on either USB connector
- Is separated from high-current wiring where practical

---

## 12. Cable Management

Route all wiring so that:

- X, Y and Z travel remain unrestricted
- Moving cables have adequate service loops
- Wires cannot touch the heated bed or hotend
- Power and signal connectors cannot be pulled by axis movement
- Cable bundles have appropriate strain relief
- High-current wiring uses secure terminations
- Cables remain identifiable for maintenance

Do not overtighten zip ties or clamps around wire insulation.

---

## 13. Power-Loss Recovery

**Power Panic is not implemented in the My-Cloner Rev A.**

Do not install a legacy Power Panic cable or board as part of the Rev A electronics assembly.

Any future power-loss-recovery implementation must be treated as a separate validated revision.

---

## 14. Pre-Power Electrical Check

Before applying mains power, verify:

- [ ] Mean Well LRS-350-24 is installed securely.
- [ ] PSU input selector is correct for the intended 230 V AC supply.
- [ ] Protective earth is connected according to the approved electrical design.
- [ ] 24 V polarity is correct.
- [ ] LM2596 output has been adjusted and measured before connecting the Raspberry Pi.
- [ ] All five TMC2209 drivers are correctly oriented.
- [ ] Motor connectors match the Rev A driver assignment.
- [ ] Heater and thermistor connections match the I/O map.
- [ ] Fan voltage is 24 V.
- [ ] No unvalidated P.I.N.D.A., filament-sensor or TS35 connection has been guessed.
- [ ] No loose conductor can contact the frame or PCB.
- [ ] All high-current terminals are secure.
- [ ] Cable routing does not interfere with moving parts.

Continue with:

[Before First Power-On](../operation/initial-setup/before-first-power-on.md)

!!! note "Physical Bring-Up"
    Final validation of driver UART communication, motor direction/current, sensorless homing, P.I.N.D.A., fans, thermistors, heaters, filament sensor and TS35 is performed during the controlled Rev A bring-up process.
