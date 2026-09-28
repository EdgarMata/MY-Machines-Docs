# Safe Usage Guidelines

The My-Cloner Rev A is an open-source FDM 3D printer that combines moving mechanical systems, electrically powered heaters and hot surfaces.

Safe operation depends not only on the machine hardware, but also on the way the printer is installed, supervised, maintained and modified.

This page describes the general precautions that should be followed when operating the completed My-Cloner.

Detailed electrical, thermal and fire-related precautions are covered in the dedicated safety pages.

---

## Intended Use

The My-Cloner is intended for additive manufacturing using compatible thermoplastic filament.

The printer should only be operated:

- Indoors
- In a dry environment
- On a stable surface
- With adequate ventilation
- With all electrical connections and components in suitable condition
- With the printer configuration appropriate for the installed hardware

Do not operate the printer if its condition is unknown following electrical, mechanical or firmware modifications.

!!! important "Open-Source Machine"
    The My-Cloner is designed to be modified and developed.

    Any modification to the electrical system, motion system, heaters, temperature sensors, firmware or safety-related configuration may change the conditions under which the machine was previously tested.

    Relevant checks must be repeated after significant modifications.

---

## Operating Environment

Install the printer in a location that provides enough space for safe operation and maintenance.

The operating area should:

- Be dry and reasonably clean
- Provide sufficient ventilation
- Have a stable and level support surface
- Keep the printer away from water and excessive humidity
- Keep combustible materials away from hot components
- Allow unrestricted movement of the printer axes
- Provide easy access to the mains connection so power can be disconnected if necessary

Do not operate the printer where objects may fall onto it or interfere with the moving components.

The printer should not be placed where its cables can create a tripping hazard or be pulled accidentally.

---

## Before Starting a Print

Before each print, perform a quick visual inspection of the machine.

Check that:

- The print surface is correctly installed
- The print area is clear
- No tools or loose objects remain inside the motion area
- Filament can feed freely
- Cables are not trapped, damaged or interfering with moving parts
- Connectors that are visible and user-accessible appear secure
- Cooling fans are unobstructed
- The nozzle and heated bed temperature readings appear plausible
- There are no obvious signs of electrical or mechanical damage

If the printer has recently been modified, repaired or reconfigured, perform the appropriate validation procedure before returning it to normal operation.

!!! warning "Unexpected Temperature Reading"
    Do not enable a heater if its reported temperature is clearly incorrect, unstable or outside a plausible ambient range.

    Investigate the temperature sensor and configuration before continuing.

---

## Safety During Operation

Remain aware of the printer while it is operating.

The printer contains:

- Rapidly moving components
- Hot surfaces
- Electrically powered heaters
- Cooling fans
- Motors and mechanical transmission components

Do not reach into the machine while an axis is moving.

Do not attempt to reposition the printhead, bed or other moving components by hand while they are under motor control.

Do not remove covers, disconnect electrical devices or modify wiring while the printer is powered.

!!! warning "Stop if Something Looks Wrong"
    Stop the printer and investigate if you observe abnormal behaviour such as:

    - Smoke
    - A burning smell
    - Sparks
    - Unexpected heating
    - Unstable temperature readings
    - Repeated thermal errors
    - Unusual mechanical noise
    - Severe vibration
    - Unexpected axis movement
    - A fan that should be operating but has stopped
    - Damaged or overheating connectors

    Disconnect mains power if necessary and safe to do so.

---

## Moving Parts

The X, Y and Z axes can move automatically and unexpectedly when commanded by firmware.

Keep hands, tools, cables and loose objects away from the motion path while the printer is active.

Particular care should be taken during:

- Homing
- Initial moves after startup
- Calibration
- Manual jogging
- Sensorless-homing tests
- Firmware configuration changes

!!! warning "Homing and Calibration"
    Homing and calibration commands may move the printer toward its mechanical limits.

    Ensure the motion area is clear before starting these procedures.

---

## Hot Surfaces

The nozzle and heated bed can remain hot for a significant time after a print has finished.

Do not touch:

- The nozzle
- Heater block
- Hotend components near the heater
- Heated bed surface

until they have cooled to a safe temperature.

Use the reported temperatures in the printer interface as a guide, but do not rely solely on the displayed value if a temperature sensor or configuration fault is suspected.

For detailed precautions, see [Electrical & Thermal Safety](electrical-and-thermal-safety.md).

---

## Supervision

A printer that is being commissioned, tested after modification, or operated with hardware or configuration that has not yet been validated should remain under direct supervision.

During normal printing:

- Periodically check the printer
- Pay attention to unusual sounds or smells
- Ensure cooling remains functional
- Ensure the print has not detached in a way that could interfere with the hotend or motion system
- Stop the print if unsafe behaviour develops

Avoid operating the printer for extended periods in situations where abnormal behaviour could go unnoticed.

!!! important "Rev A Validation"
    Hardware or configuration marked as **Pending validation** should not be treated as fully validated simply because the printer powers on or begins printing.

---

## Children and Pets

The printer is not a toy.

Children and pets should not have unsupervised access to the printer, especially while it is:

- Heating
- Printing
- Homing
- Cooling after a print

Hot surfaces and automatic motion can remain hazardous even when the printer appears idle.

---

## Tools and Part Removal

Use suitable tools when removing printed parts or performing routine maintenance.

When using a scraper, knife or similar tool:

- Work away from your body where practical
- Keep the other hand away from the tool path
- Avoid excessive force
- Allow the print surface to cool if this helps release the part safely

Take additional care when cutting supports, trimming filament or post-processing printed parts.

Safety glasses are recommended when cutting, drilling, sanding or working on parts that may produce fragments.

---

## Abnormal Behaviour

Stop using the printer if it develops a condition that may affect safe operation.

Examples include:

- Damaged wiring
- Loose electrical connectors
- Intermittent power
- Repeated controller resets
- Heater faults
- Thermistor errors
- Unexpected temperature changes
- Failed cooling fans
- Grinding or binding motion
- Repeated sensorless-homing failures
- Unexpected probe behaviour
- Unusual smells, smoke or discoloration

Do not repeatedly clear firmware safety errors without identifying their cause.

Safety mechanisms are intended to identify conditions that require investigation.

---

## Modifications and Revalidation

The My-Cloner is an open-source machine and may be modified by its owner.

Changes to the following systems can affect previous validation:

- Main controller
- Stepper drivers
- Motors
- Homing configuration
- Z probe
- Hotend
- Heater cartridge
- Thermistors
- Heated bed
- Cooling fans
- Power supply
- DC power conversion
- Wiring
- Klipper configuration

After a significant modification, repeat the checks relevant to the affected subsystem before returning the printer to normal operation.

Examples include:

- Motor-direction testing after changing motor wiring
- Temperature verification after changing a thermistor
- Heater checks after replacing a heater
- Fan testing after changing fan wiring or configuration
- Homing validation after changing TMC2209 settings
- Probe validation after changing the Z-probe configuration

Do not assume that configuration values from another printer or an earlier My-Cloner revision are safe for the current hardware.

---

## After Printing

After a print has finished:

1. Allow the hotend and heated bed to cool.
2. Remove the printed part using appropriate tools if required.
3. Inspect the print area for loose filament or debris.
4. Check that nothing is obstructing the motion system.
5. Investigate any abnormal behaviour observed during the print before starting another job.

If maintenance or electrical work is required, disconnect the printer from the mains supply before beginning the work.

---

## Related Documentation

- [Electrical & Thermal Safety](electrical-and-thermal-safety.md) — electrical hazards, heaters, temperature monitoring and hot surfaces
- [Fire & Environment Safety](fire-and-environment-safety.md) — fire prevention, ventilation and operating environment
- [Wiring & Electronics](../wiring/index.md) — My-Cloner Rev A electrical architecture and connections
- [Before First Power-On](../operation/initial-setup/before-first-power-on.md) — pre-power inspection before commissioning or electrical changes
- [First Power-On](../operation/initial-setup/first-power-on.md) — controlled initial power-up procedure