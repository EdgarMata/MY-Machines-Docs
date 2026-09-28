# Electrical and Thermal Safety

The My-Cloner Rev A combines mains-powered electrical equipment, 24 V DC electronics, high-current heaters and surfaces capable of reaching temperatures that can cause burns or damage.

This page describes the electrical and thermal precautions that apply when operating, inspecting or maintaining the completed printer.

Detailed wiring and commissioning procedures are documented separately.

---

## Mains Voltage

The My-Cloner Rev A contains **230 V AC mains wiring** inside the electrical system.

Mains voltage is present around the IEC inlet, power switch, fuse, power-supply input terminals and associated wiring.

!!! danger "Mains Voltage"
    Contact with mains voltage can cause serious injury or death.

    Do not open, inspect, reconnect or modify mains wiring while the printer is connected to the power outlet.

Before accessing any mains-powered part of the printer:

1. Stop the printer.
2. Switch the printer off.
3. Disconnect the mains plug from the wall outlet.
4. Confirm that the machine cannot be powered accidentally.

The printer's external power switch must not be treated as a substitute for physically disconnecting the mains plug when electrical work is required.

---

## Protective Earth

The My-Cloner Rev A electrical architecture includes protective-earth connections.

Protective earth is a safety conductor and must not be removed, bypassed or replaced by the DC negative conductor.

!!! danger "Protective Earth"
    Do not operate the printer if a protective-earth connection is known or suspected to be damaged, disconnected or incorrectly installed.

If the protective-earth system has been modified or repaired, the printer should not return to normal operation until the relevant electrical checks have been completed.

For the electrical architecture, see [Power Distribution](../wiring/power-distribution.md).

---

## Power Cord and Mains Connection

Inspect the mains cable and external connection periodically.

Do not operate the printer if:

- The mains cable is cut, crushed or damaged
- The plug is damaged
- The IEC connector is loose
- The power inlet is damaged
- There are signs of overheating or discoloration
- The cable or connector becomes unusually hot during operation

Position the cable so that it cannot:

- Become trapped by the printer
- Contact hot components
- Interfere with moving parts
- Create a tripping hazard
- Be pulled accidentally

When disconnecting the printer, pull the plug or connector body rather than pulling directly on the cable.

---

## Low-Voltage Electrical System

Most of the printer operates from a **24 V DC system**, with a separate **5 V DC supply for the Raspberry Pi Zero 2 W**.

Although these voltages are substantially lower than mains voltage, incorrect wiring or damaged connections can still cause:

- Short circuits
- Connector overheating
- Damaged electronics
- Failed fans
- Heater faults
- Fire risk

Do not continue operating the printer if a connector, cable or terminal shows signs of overheating or damage.

!!! warning "Electrical Damage"
    A low-voltage circuit should not be assumed to be harmless simply because it is not connected directly to mains voltage.

    High-current 24 V circuits, particularly heater circuits, require correctly rated wiring and secure connections.

---

## Hotend and Heated Bed

The printer contains two electrically powered heating systems:

- Hotend heater
- Heated bed

Both can reach temperatures capable of causing burns.

!!! danger "Hot Surfaces"
    Do not touch the nozzle, heater block or heated bed while they are hot.

    Allow the printer to cool before touching heated components or beginning maintenance.

The hotend may remain hot for several minutes after heating has stopped.

The heated bed may also remain hot after a print has finished.

Do not assume that a component is safe to touch simply because the printer is idle.

---

## Temperature Readings

The printer relies on temperature sensors to control the hotend and heated bed.

The displayed temperature should behave plausibly before and during heating.

Before enabling a heater, check that its reported temperature is reasonable for the surrounding environment.

Examples of suspicious behaviour include:

- Temperature far above or below ambient temperature while cold
- Large unexplained temperature jumps
- Rapid fluctuations while the printer is stationary
- A fixed temperature that does not respond to heating
- Sudden temperature loss during operation

!!! warning "Unexpected Temperature Reading"
    Do not enable a heater if its reported temperature appears incorrect or unstable.

    Stop and investigate the sensor, wiring and configuration before continuing.

A valid MCU input pin alone does not confirm that the installed thermistor type or configuration is correct.

---

## Heater Safety

A heater must only operate while its associated temperature sensor is connected, configured and reporting correctly.

!!! danger "Never Power an Unmonitored Heater"
    Do not operate a heater without valid temperature feedback.

    A heater operating without reliable temperature monitoring can overheat uncontrollably.

Do not bypass heater errors simply to continue a print.

Repeated heater errors may indicate:

- Loose heater wiring
- Damaged thermistor wiring
- Incorrect thermistor configuration
- Heater failure
- Connector problems
- Insufficient heater power
- Excessive cooling
- Incorrect firmware limits

The cause should be identified before returning the printer to normal operation.

---

## Thermal Protection

Klipper provides temperature monitoring and heater safety mechanisms.

These protections are part of the printer's safety system and should remain enabled.

!!! danger "Never Disable Thermal Protection"
    Do not disable temperature monitoring, heater verification or other thermal-safety mechanisms to bypass a fault.

A thermal error should be treated as an indication that something requires inspection.

Firmware settings must correspond to the actual heater and temperature-sensor hardware installed in the machine.

For the current Rev A thermal architecture, see [Heaters & Temperature Sensors](../wiring/heaters-and-temperature-sensors.md).

---

## Hotend Cooling

The My-Cloner Rev A uses a dedicated hotend cooling fan.

Adequate heatsink cooling is required when the hotend operates at printing temperatures.

!!! important "Hotend Cooling"
    Do not continue heating the hotend if the required hotend cooling fan is not operating correctly.

A failed or obstructed hotend fan can cause excessive heat transfer into the cold side of the hotend and may result in:

- Heat creep
- Filament softening above the intended melt zone
- Extrusion jams
- Unstable printing
- Excessive heating of nearby components

If the fan stops unexpectedly while the hotend is hot, stop the print and allow the system to cool before investigating.

For fan configuration and assignments, see [Fans](../wiring/fans.md).

---

## Electrical and Thermal Inspection

Stop using the printer if you observe:

- Burning smell
- Smoke
- Sparks
- Discoloration around terminals or connectors
- Melted insulation
- Loose electrical connections
- Repeated power interruptions
- Unusual heating of cables or connectors
- Heater temperatures that cannot be controlled
- Thermistor errors
- Failed hotend cooling
- Repeated firmware thermal faults

!!! warning "Stop and Investigate"
    Do not repeatedly restart the printer after an electrical or thermal fault without identifying the cause.

If smoke, fire or another immediate hazard develops, disconnect mains power only if it is safe to do so.

See [Fire & Environment Safety](fire-and-environment-safety.md) for fire-related precautions.

---

## After Maintenance or Modification

Electrical or thermal modifications may change the conditions under which the printer was previously validated.

Relevant checks should be repeated after changes to:

- Power supply
- Wiring
- Controller board
- Heater cartridge
- Heated bed
- Thermistors
- Cooling fans
- Connectors
- Klipper heater configuration
- Temperature limits
- Fan control

Examples include:

- Verifying temperature readings after changing a thermistor
- Testing heater behaviour after replacing a heater
- Checking fan operation after changing fan wiring
- Repeating electrical inspection after rewiring a power circuit

Do not return the printer to unattended or extended operation immediately after significant electrical or thermal changes.

---

## Before Returning to Normal Operation

After electrical or thermal maintenance, confirm that:

- No loose tools or conductive objects remain inside the printer
- Cables are secure
- Connectors are fully seated
- No insulation has been damaged
- Cooling fans operate as intended
- Temperature readings are plausible
- Heaters respond correctly
- No connector becomes unusually hot
- No firmware safety errors occur

If mains wiring, the power supply or the main power architecture has been changed, follow the appropriate commissioning procedure rather than performing a normal print immediately.

---

## Internal PSU Service

!!! danger "Do Not Open the PSU"
    The PSU contains mains-voltage circuitry and internal components that may retain charge after disconnection.

    Do not open or repair the power supply unless you are qualified to service mains-powered equipment.

Replace a damaged or suspect PSU with a suitable unit matching the approved Rev A specification.

---

## Related Documentation

- [Safe Usage Guidelines](safe-usage.md) — general operating precautions
- [Fire & Environment Safety](fire-and-environment-safety.md) — fire prevention, ventilation and operating environment
- [Power Distribution](../wiring/power-distribution.md) — My-Cloner Rev A mains, 24 V and 5 V architecture
- [Heaters & Temperature Sensors](../wiring/heaters-and-temperature-sensors.md) — heater and thermistor configuration
- [Fans](../wiring/fans.md) — hotend and part-cooling systems
- [Before First Power-On](../operation/initial-setup/before-first-power-on.md) — controlled inspection before initial or renewed commissioning
- [First Power-On](../operation/initial-setup/first-power-on.md) — staged initial power-up procedure