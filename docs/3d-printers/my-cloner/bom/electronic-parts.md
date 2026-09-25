# Electronic Parts

This page lists the electrical and electronic components required to build the **My-Cloner Rev A**.

The My-Cloner Rev A uses a **24 V DC electrical architecture**, with a Raspberry Pi Zero 2 W running Klipper and an MKS Robin Nano V3 controlling the printer hardware.

!!! info "Authoritative BOM"
    The **My-Cloner Rev A BOM V2** is the authoritative Bill of Materials for this hardware revision.

    Purchase links are provided for convenience and may include affiliate links. Equivalent components may be used when they meet the specifications listed in the BOM.

## Control Electronics

| Qty | Component | Specification | Amazon | AliExpress |
|:---:|---|---|:---:|:---:|
| 1 | MKS Robin Nano V3 Controller Board | 24 V DC main system supply | [Amazon](https://amzn.to/3ZCNnzE) | [AliExpress](https://s.click.aliexpress.com/e/_oFuFnJq) |
| 1 | Raspberry Pi Zero 2 W | Klipper host | — | — |
| 1 | MKS TS35 V2.0 Display | Connected through the controller interface | [Amazon](https://amzn.to/3ZCNnzE) | [AliExpress](https://s.click.aliexpress.com/e/_oFuFnJq) |
| 1 | LM2596 DC-DC Step-Down Converter | 24 V DC input → 5 V DC output for Raspberry Pi | — | — |
| 5 | TMC2209 Stepper Driver | StepStick-compatible, UART mode, DIAG pin available, compatible with MKS Robin Nano V3 | — | — |

!!! note "Display Integration"
    The MKS TS35 V2.0 is part of the My-Cloner Rev A hardware configuration.

    Its final integration with the Klipper-based system is still being validated. **Mainsail remains the primary printer interface.**

---

## Power System

| Qty | Component | Specification | Amazon | AliExpress |
|:---:|---|---|:---:|:---:|
| 1 | MEAN WELL LRS-350-24 Power Supply | 24 V DC, 14.6 A, 350.4 W | [Amazon](https://amzn.to/4l9XvrV) | [AliExpress](https://s.click.aliexpress.com/e/_oCkcgSg) |
| 1 | IEC C14 Mains Inlet | Integrated switch and fuse | [Amazon](https://amzn.to/4ne2VUL) | [AliExpress](https://s.click.aliexpress.com/e/_oCrQwoc) |

!!! warning "Mains Voltage"
    The power supply and IEC inlet are connected to AC mains voltage.

    Mains wiring must follow the My-Cloner wiring documentation and applicable electrical safety requirements.

    Never work on mains wiring while the printer is connected to a power outlet.

---

## Motion System

The My-Cloner uses five stepper motors.

| Qty | Component | Function | Amazon | AliExpress |
|:---:|---|---|:---:|:---:|
| 1 | NEMA 17 Stepper Motor | X axis | [Amazon](https://amzn.to/4kP6lf0) | [AliExpress](https://s.click.aliexpress.com/e/_on92auc) |
| 1 | NEMA 17 Stepper Motor | Y axis | [Amazon](https://amzn.to/4kP6lf0) | [AliExpress](https://s.click.aliexpress.com/e/_on92auc) |
| 1 | NEMA 17 Stepper Motor | Left Z axis | [Amazon](https://amzn.to/4kP6lf0) | [AliExpress](https://s.click.aliexpress.com/e/_on92auc) |
| 1 | NEMA 17 Stepper Motor | Right Z axis | [Amazon](https://amzn.to/4kP6lf0) | [AliExpress](https://s.click.aliexpress.com/e/_on92auc) |
| 1 | NEMA 17 Pancake Stepper Motor | Direct-drive extruder | [Amazon](https://amzn.to/3SS62Um) | [AliExpress](https://s.click.aliexpress.com/e/_oCEGMP6) |

### Stepper Drivers

The My-Cloner Rev A uses **5 × TMC2209 stepper drivers**.

The drivers are intended to operate in **UART mode** with the MKS Robin Nano V3.

Sensorless homing is planned for the **X and Y axes** using the TMC2209 DIAG outputs.

The Z axis uses the P.I.N.D.A. probe for Z referencing.

---

## Heated Bed

| Qty | Component | Specification | Amazon | AliExpress |
|:---:|---|---|:---:|:---:|
| 1 | Heated Bed | 230 × 230 mm, 24 V DC | [Amazon](https://amzn.to/4la2xVc) | [AliExpress](https://s.click.aliexpress.com/e/_olKRKYM) |
| 1 | Heated Bed Thermistor | Compatible with the heated bed and Klipper configuration | — | — |

The removable spring steel sheet and PEI print surface are mechanical/build-surface components and are listed in the [Mechanical Parts](mechanical-parts.md) BOM.

---

## Hotend Electronics

The My-Cloner Rev A uses a V6-style hotend.

| Qty | Component | Specification |
|:---:|---|---|
| 1 | Heater Cartridge | 24 V DC |
| 1 | Hotend Thermistor | Compatible with the V6 heater block and Klipper configuration |

The remaining mechanical hotend components are defined separately in the engineering BOM.

!!! note "Thermistor Specification"
    The exact hotend thermistor model must match the Klipper configuration.

    Do not substitute a different thermistor type without updating and validating the firmware configuration.

---

## Cooling

| Qty | Component | Specification | Amazon | AliExpress |
|:---:|---|---|:---:|:---:|
| 1 | 4010 Axial Fan | 24 V DC — hotend cooling | [Amazon](https://amzn.to/4l9BObn) | [AliExpress](https://s.click.aliexpress.com/e/_oCuAsFy) |
| 1 | 5015 Blower Fan | 24 V DC — part cooling | [Amazon](https://amzn.to/4472GSH) | [AliExpress](https://s.click.aliexpress.com/e/_oFIKbT0) |

!!! warning "24 V Fans"
    The My-Cloner Rev A uses **24 V fans**.

    Earlier My-Cloner documentation referenced 12 V fans. Those references are obsolete and must not be used for Rev A.

---

## Sensors

| Qty | Component | Specification | Amazon | AliExpress |
|:---:|---|---|:---:|:---:|
| 1 | P.I.N.D.A. Probe | Inductive Z probe | [Amazon](https://amzn.to/4n7H29s) | [AliExpress](https://s.click.aliexpress.com/e/_omTpVJA) |
| 1 | IR Filament Sensor | MK3-style IR sensor with mechanical ball and magnet mechanism | [Amazon](https://amzn.to/4jYzFhV) | [AliExpress](https://s.click.aliexpress.com/e/_oBvssJ8) |

---

## Electrical Architecture

The main power architecture of the My-Cloner Rev A is:

    AC Mains
        │
        ▼
    IEC C14 Inlet
    Switch + Fuse
        │
        ▼
    MEAN WELL LRS-350-24
        │
        └── 24 V DC
            │
            ├── MKS Robin Nano V3
            ├── Heated Bed
            ├── Hotend Heater
            ├── 4010 Hotend Fan
            ├── 5015 Part Cooling Fan
            │
            └── LM2596
                 │
                 └── 5 V DC
                     │
                     └── Raspberry Pi Zero 2 W

For connector locations, wire routing and electrical assembly, refer to the [Wiring & Electronics](../wiring/index.md) documentation.

## Complete BOM

For the complete engineering Bill of Materials, including references and revision-controlled component information, see:

[:octicons-arrow-right-24: BOM Downloads](../downloads/bom-files.md){ .md-button .md-button--primary }