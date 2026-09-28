# Glossary of Common Terms

This glossary explains common 3D printing and My-Cloner terms used throughout the documentation.

---

## 3D Printing Terms

### Bed / Heatbed

The heated build platform where the printed part is created.

On the My-Cloner, the heatbed supports the removable spring steel print sheet.

---

### Bed Mesh

A measured map of the print surface created by probing multiple points across the bed.

Klipper can use this mesh to compensate for small variations in the bed surface during printing.

---

### Brim

An additional single-layer area printed around the base of a model.

A brim can improve bed adhesion and help reduce warping.

---

### Extruder

The mechanism that feeds filament toward the hotend.

The My-Cloner uses a direct-drive extruder.

---

### Filament

The thermoplastic material used by the printer.

The My-Cloner uses **1.75 mm filament**.

Common materials include:

- PLA
- PETG
- ABS
- ASA

---

### First Layer

The first printed layer of a model.

A correct first layer is critical for:

- Bed adhesion
- Dimensional stability
- Print reliability

The first layer is strongly affected by the Z offset, bed mesh and print surface condition.

---

### G-code

The machine instruction format used by 3D printers.

The slicer converts a 3D model into G-code containing movement, temperature, extrusion and other printer commands.

---

### Hotend

The assembly responsible for heating and melting filament.

It typically includes:

- Heatsink
- Heatbreak
- Heater block
- Heater cartridge
- Thermistor
- Nozzle

The My-Cloner Rev A uses a V6-style hotend.

---

### Layer Height

The vertical thickness of each printed layer.

Smaller layer heights generally provide finer detail, while larger layer heights can reduce print time.

---

### Nozzle

The final part of the hotend through which molten filament is extruded.

The standard My-Cloner nozzle size is:

**0.4 mm**

---

### Overhang

A part of a model that extends outward without material directly underneath it.

Large overhangs may require cooling, slower print settings or support material.

---

### Retraction

The controlled backward movement of filament used to reduce nozzle pressure during travel moves.

Retraction can help reduce stringing.

---

### Slicer

Software that converts a 3D model into G-code for the printer.

The recommended slicer for the My-Cloner is:

**OrcaSlicer**

---

### STL

A common file format used for 3D models.

STL files describe model geometry but do not contain printer settings.

---

### Stringing

Thin strands of filament that form between separate areas of a print.

Stringing is commonly influenced by:

- Temperature
- Retraction
- Travel settings
- Filament condition

---

### Support

Additional printed structures used to support parts of a model that cannot be printed directly in open air.

Supports are removed after printing.

---

### Warping

A print defect where part of the model lifts away from the print surface.

Warping can be influenced by:

- Bed adhesion
- Bed temperature
- Material shrinkage
- Ambient temperature
- Cooling

---

## My-Cloner and Klipper Terms

### Endstop

A mechanism used by firmware to detect a reference or limit position of an axis.

On the My-Cloner Rev A, X and Y do **not** use physical endstop switches. Their endstop function is provided by the TMC2209 sensorless-homing system using StallGuard / DIAG signals.

---

### Firmware

Software responsible for controlling the printer hardware.

The My-Cloner uses **Klipper**.

---

### Host

The computer running the main Klipper software.

On the My-Cloner Rev A, the host is the:

**Raspberry Pi Zero 2 W**

---

### Homing

The process of establishing a known reference position for the printer axes.

On the My-Cloner Rev A:

- X uses TMC2209 sensorless homing.
- Y uses TMC2209 sensorless homing.
- Z uses the P.I.N.D.A. probe for its reference.

---

### Klipper

The firmware used by the My-Cloner.

Klipper divides printer control between:

- A host computer
- A printer mainboard acting as an MCU

This architecture allows advanced motion control, configuration and calibration features.

---

### Mainsail

The primary web interface used to control the My-Cloner.

Mainsail provides access to:

- Printer status
- Movement controls
- Temperature controls
- G-code files
- Calibration commands
- Klipper console
- Print monitoring

---

### MCU

**Microcontroller Unit**

In the My-Cloner Klipper architecture, the MCU is the printer mainboard:

**MKS Robin Nano V3**

The MCU handles real-time control of the printer hardware based on commands from the Klipper host.

---

### P.I.N.D.A.

The inductive probe used by the My-Cloner to detect the print bed.

It is used for functions including:

- Z homing
- Z-offset calibration
- Bed mesh measurement

---

### Probe

A sensor used to detect the print bed without direct nozzle contact.

The My-Cloner Rev A uses a **P.I.N.D.A. probe**.

---

### Raspberry Pi

A small single-board computer.

The My-Cloner uses a **Raspberry Pi Zero 2 W** as the Klipper host.

---

### Z Offset

The calibrated vertical distance between the probe trigger position and the nozzle.

The Z offset determines the nozzle height relative to the print surface.

Correct Z-offset calibration is essential for a good first layer.

---

## Hardware Terms

### Heatbed

The electrically heated build platform.

The My-Cloner Rev A uses a:

**235 × 235 mm, 24 V, 220 W Ender 3-type heatbed**

---

### LM2596

A DC-DC step-down converter used in the My-Cloner electrical system.

It converts:

**24 V DC → 5 V DC**

The 5 V output is used to power the Raspberry Pi Zero 2 W.

---

### Mainboard

The main electronics controller of the printer.

The My-Cloner Rev A uses:

**MKS Robin Nano V3**

---

### NEMA 17

A commonly used stepper motor frame size in 3D printers.

The My-Cloner uses NEMA 17 motors for its motion and extrusion systems.

---

### PEI

**Polyetherimide**

A material commonly used as a 3D printing surface.

The My-Cloner uses a removable spring steel sheet with a smooth PEI surface.

---

### PSU

**Power Supply Unit**

The PSU converts mains AC voltage into the DC voltage used by the printer.

The My-Cloner Rev A uses:

**Mean Well LRS-350-24**

---

### Spring Steel Sheet

A removable flexible print surface.

After the print cools, the sheet can be removed and flexed to help release the printed part.

The My-Cloner uses a smooth PEI-coated spring steel sheet.

---

### Stepper Motor

A motor that moves in controlled increments.

Stepper motors are used by the My-Cloner for:

- X-axis movement
- Y-axis movement
- Z-axis movement
- Filament extrusion

---

### Thermistor

A temperature-sensitive electrical component used to measure temperature.

The My-Cloner uses thermistors to monitor the hotend and heated bed.

---

## Calibration Terms

### Bed Mesh Calibration

The process of measuring multiple points across the print surface using the Z probe.

In Klipper, this can be started using:

    BED_MESH_CALIBRATE

---

### PID Tuning

A calibration process used to improve temperature stability.

PID tuning can be performed for:

- Hotend
- Heated bed

---

### Probe Calibration

The process used to determine the correct relationship between the Z probe and nozzle.

In Klipper, this can be started using:

    PROBE_CALIBRATE

---

### SAVE_CONFIG

A Klipper command used to save supported calibration results to the printer configuration.

After certain calibration procedures, run:

    SAVE_CONFIG

---

## Software Terms

### OrcaSlicer

The recommended slicing software for the My-Cloner.

OrcaSlicer converts 3D models into G-code using the configured My-Cloner machine and print profiles.

---

### Printer Profile

A slicer configuration containing machine-specific information such as:

- Build volume
- Nozzle size
- Machine limits
- G-code configuration
- Printer capabilities

Use the official MyMachines My-Cloner profile whenever available.

---

### Print Profile

A slicer configuration containing settings related to print quality and behaviour.

Examples include:

- Layer height
- Speed
- Acceleration
- Retraction
- Infill
- Supports

---

### Filament Profile

A slicer configuration containing material-specific settings.

Examples include:

- Nozzle temperature
- Bed temperature
- Cooling
- Flow
- Maximum volumetric speed

Different filament materials should use appropriate filament profiles.