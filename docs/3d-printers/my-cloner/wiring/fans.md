# My-Cloner Rev A — Fans

This page documents the cooling fans used by the **My-Cloner Rev A** and their connection to the MKS Robin Nano V3.

The printer uses two 24 V cooling fans:

- 1 × 4010 axial fan for hotend heatsink cooling
- 1 × 5015 blower fan for part cooling

!!! warning "24 V Fans"
    The My-Cloner Rev A uses **24 V fans**.

    Earlier project documentation referenced 12 V fans. Those references are obsolete and must not be used for Rev A.

---

## Cooling Architecture

The My-Cloner Rev A uses two independent cooling functions:

| Function | Fan Type | Voltage |
|---|---|---:|
| Hotend heatsink cooling | 4010 axial fan | 24 V DC |
| Part cooling | 5015 blower fan | 24 V DC |

The MKS Robin Nano V3 provides two controllable fan outputs.

| Board Output | MCU Pin | My-Cloner Assignment |
|---|---:|---|
| FAN1 | `PC14` | TBD |
| FAN2 | `PB1` | TBD |

The board-level pin mapping is confirmed by the official Robin Nano V3 documentation and Klipper configuration.

The final assignment between FAN1/FAN2 and the physical 4010/5015 fans will be defined during wiring validation.

---

## Hotend Cooling Fan

The hotend uses a:

**4010 axial fan — 24 V DC**

Its purpose is to cool the hotend heatsink and reduce heat creep.

| Item | Specification |
|---|---|
| Fan type | Axial |
| Size | 40 × 40 × 10 mm |
| Voltage | 24 V DC |
| Function | Hotend heatsink cooling |
| Board output | TBD |
| MCU pin | TBD |

The final electrical assignment will be either FAN1 or FAN2.

!!! important "Hotend Cooling"
    The hotend cooling fan is a critical part of the hotend thermal system.

    The hotend should not be operated at extrusion temperatures without adequate heatsink cooling.

---

## Part-Cooling Fan

The My-Cloner Rev A uses a:

**5015 blower fan — 24 V DC**

Its purpose is to provide controlled airflow to the printed part.

| Item | Specification |
|---|---|
| Fan type | Radial blower |
| Size | 50 × 50 × 15 mm |
| Voltage | 24 V DC |
| Function | Part cooling |
| Board output | TBD |
| MCU pin | TBD |

The final electrical assignment will be either FAN1 or FAN2.

---

## MKS Robin Nano V3 Fan Outputs

The Robin Nano V3 provides two MOSFET-controlled fan outputs.

| Output | MCU Pin |
|---|---:|
| FAN1 | `PC14` |
| FAN2 | `PB1` |

The official generic Klipper configuration uses `PC14` as the example primary fan output and lists `PB1` as the second available output.

The My-Cloner does not need to preserve that exact functional assignment.

The physical wiring and final Klipper configuration must agree with each other.

---

## Final Fan Assignment

The final Rev A assignment is currently pending.

The intended result will be documented as:

| Function | Fan | Board Output | MCU Pin | Klipper Section |
|---|---|---|---:|---|
| Hotend cooling | 4010 | TBD | TBD | TBD |
| Part cooling | 5015 | TBD | TBD | `[fan]` |

!!! note "Pending Wiring Decision"
    The board pins are known, but the functional assignment is intentionally left open until the final wiring is confirmed.

    Once validated, this table should become the authoritative fan mapping for Rev A.

---

## Klipper Configuration

The part-cooling fan will normally be controlled by Klipper using a `[fan]` section.

The final configuration will follow the selected Robin Nano output.

Example structure:

    [fan]
    pin: <FAN_OUTPUT_PIN>

The hotend heatsink fan may use an automatically controlled Klipper configuration.

A typical structure is:

    [heater_fan hotend_fan]
    pin: <FAN_OUTPUT_PIN>
    heater: extruder

The final parameters must be validated on the physical printer.

!!! warning "Example Only"
    The configuration above describes the intended structure only.

    Do not copy placeholder pins into the final `printer.cfg`.

---

## Fan Polarity

Before connecting a fan, confirm:

- Rated voltage
- Positive conductor
- Negative conductor
- Connector orientation
- Robin Nano output polarity

Do not assume wire colours are consistent between different fan manufacturers.

!!! warning "Verify Before Power-On"
    Reversed polarity may prevent the fan from operating and may damage some electronic fan assemblies.

    Verify polarity before applying power.

---

## Fan Control Validation

Each fan should be tested independently during bring-up.

### 4010 Hotend Fan

Verify that:

1. The fan connected is the 24 V 4010 fan.
2. The selected board output matches the Klipper configuration.
3. The fan spins freely.
4. Airflow is directed through the hotend heatsink.
5. The fan activates at the intended hotend temperature.
6. The fan stops or behaves as configured when the hotend cools.

### 5015 Part-Cooling Fan

Verify that:

1. The fan connected is the 24 V 5015 blower.
2. The selected board output matches the Klipper configuration.
3. The blower spins freely.
4. Airflow reaches the intended nozzle/part-cooling duct.
5. Klipper can vary fan speed.
6. `0%` results in the expected off state.
7. `100%` results in full-speed operation.

---

## PWM Testing

The part-cooling fan should be tested at several command levels.

Suggested validation points:

- 0%
- 25%
- 50%
- 75%
- 100%

Observe:

- Reliable fan startup
- Stable operation
- Noise or vibration
- Airflow
- Whether a minimum usable PWM value is required

Some fans may not start reliably at very low PWM values.

If necessary, the final Klipper configuration can be adjusted after physical testing.

---

## Wiring Considerations

Fan wiring should:

- Use secure connectors
- Include suitable strain relief
- Avoid contact with moving parts
- Avoid hot surfaces
- Allow normal toolhead movement
- Match the selected board output
- Remain clearly identifiable during maintenance

The toolhead fan cables should be routed with the rest of the moving hotend wiring without restricting X-axis movement.

---

## Failure Considerations

### Hotend Fan Failure

A failed hotend cooling fan may cause excessive heat transfer into the cold side of the hotend.

Possible symptoms include:

- Heat creep
- Filament softening above the melt zone
- Extrusion jams
- Unstable extrusion

If the hotend fan stops unexpectedly, printing should be stopped and the cause investigated.

### Part-Cooling Fan Failure

A failed part-cooling fan normally does not create the same thermal risk to the hotend, but may significantly affect print quality.

Possible effects include:

- Poor bridging
- Poor overhangs
- Reduced small-layer cooling
- Dimensional problems on some materials

---

## Validation Status

| Item | Status |
|---|---|
| 4010 fan type | Defined |
| 4010 voltage | Defined — 24 V |
| 5015 fan type | Defined |
| 5015 voltage | Defined — 24 V |
| FAN1 MCU pin | Source confirmed — `PC14` |
| FAN2 MCU pin | Source confirmed — `PB1` |
| 4010 board-output assignment | Pending validation |
| 5015 board-output assignment | Pending validation |
| Hotend fan Klipper section | Pending configuration |
| Part-cooling Klipper section | Pending configuration |
| PWM behaviour | Pending physical validation |
| Fan airflow direction | Pending physical validation |

---

## Related Documentation

For the complete electrical mapping:

[I/O Map](io-map.md)

For controller information:

[Controller Board](controller-board.md)

For heater and thermal-system information:

[Heaters & Temperature Sensors](heaters-and-temperature-sensors.md)

For the future Klipper configuration:

[Firmware Configuration](../downloads/firmware-configuration.md)