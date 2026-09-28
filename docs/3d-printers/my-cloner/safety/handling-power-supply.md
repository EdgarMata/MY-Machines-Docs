# Handling the Power Supply

The **My-Cloner Rev A** uses a **Mean Well LRS-350-24** power supply.

It converts the intended **230 V AC mains input** into the printer's **24 V DC main power rail**.

!!! danger "Mains Voltage"
    The AC side of the power supply operates at hazardous mains voltage.

    Disconnect the printer from the power outlet before opening the electronics area, changing wiring or touching PSU terminals.

---

## Input Voltage Selector

The Mean Well LRS-350-24 uses a selectable AC input range.

For the standard My-Cloner Rev A configuration documented here, the intended mains supply is:

**230 V AC**

!!! danger "Check Before First Power-On"
    Verify the PSU input-voltage selector before connecting mains power.

    Do not assume that the selector is in the correct position when the PSU is received or after maintenance.

---

## Protective Earth

Protective earth must be connected according to the approved My-Cloner Rev A electrical design.

The protective-earth connection must not be replaced by the 24 V DC negative conductor.

Any exposed conductive parts that require protective grounding must be bonded as defined by the electrical schematic.

---

## Power Connections

Before applying mains power, verify:

- AC live and neutral are connected to the correct PSU input terminals.
- Protective earth is correctly connected.
- 24 V DC output polarity is correct.
- All terminals are securely tightened.
- No loose conductor strands are exposed.
- Cable insulation is undamaged.
- Wiring cannot contact sharp edges or moving parts.
- The PSU input selector is correct for the intended mains supply.

Do not identify terminals by their physical order alone. Follow the markings on the installed PSU and the current [Power Distribution](../wiring/power-distribution.md) documentation.

---

## Power Cord and IEC Inlet

The My-Cloner Rev A uses an IEC C14 mains inlet with integrated switch and fuse.

Use a mains cable suitable for the local supply and the printer's electrical load.

Inspect the cable and inlet regularly for:

- Cuts
- Cracked insulation
- Loose contacts
- Heat damage
- Mechanical damage

When disconnecting the printer, pull the plug or connector body rather than the cable.

---

## Internal PSU Service

!!! danger "Do Not Open the PSU"
    The PSU contains mains-voltage circuitry and internal components that may retain charge after disconnection.

    Do not open or repair the power supply unless you are qualified to service mains-powered equipment.

Replace a damaged or suspect PSU with a suitable unit matching the approved Rev A specification.

---

## Before First Power-On

The complete staged electrical check is documented in:

[Before First Power-On](../operation/initial-setup/before-first-power-on.md)

For the current AC and DC architecture:

[Power Distribution](../wiring/power-distribution.md)
