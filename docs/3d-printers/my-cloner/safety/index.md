# Safety Guidelines

The My-Cloner Rev A is an open-source FDM 3D printer that combines electrically powered heaters, moving mechanical systems, cooling fans and mains-powered equipment.

Safe operation depends on using the machine in a suitable environment, keeping its safety systems active and responding appropriately to abnormal behaviour.

This section focuses on the precautions that apply when **operating the completed printer**.

Assembly-specific risks, wiring procedures and first-power-on checks are documented separately in the relevant assembly, wiring and initial-setup sections.

!!! important "Safety Depends on Multiple Layers"
    Safe operation should never depend on a single protection mechanism.

    Electrical design, temperature monitoring, firmware protection, cooling, inspection, supervision and a suitable operating environment all contribute to reducing risk.

---

## Safety Topics

<div class="grid cards" markdown>

-   :material-shield-check:{ .lg .middle } **Safe Usage Guidelines**

    ---

    General precautions for operating the My-Cloner safely, including supervision, moving parts, tools, modifications and abnormal behaviour.

    [:octicons-arrow-right-24: Read Safe Usage Guidelines](safe-usage.md)

-   :material-flash-alert:{ .lg .middle } **Electrical & Thermal Safety**

    ---

    Electrical hazards, mains voltage, hot surfaces, heaters, temperature sensors, thermal protection and cooling requirements.

    [:octicons-arrow-right-24: Read Electrical & Thermal Safety](electrical-and-thermal-safety.md)

-   :material-fire-alert:{ .lg .middle } **Fire & Environment Safety**

    ---

    Fire prevention, smoke detection, fire-response preparation, ventilation, flammable materials, long prints and safe printer placement.

    [:octicons-arrow-right-24: Read Fire & Environment Safety](fire-and-environment-safety.md)

</div>

---

## Recommended Reading

Before operating the printer for the first time, read all three safety pages.

A practical reading order is:

1. [Safe Usage Guidelines](safe-usage.md)
2. [Electrical & Thermal Safety](electrical-and-thermal-safety.md)
3. [Fire & Environment Safety](fire-and-environment-safety.md)

These pages are intended to be read together.

---

## Stop and Investigate

Do not continue operating the printer if you observe behaviour that may indicate an electrical, thermal or mechanical fault.

Examples include:

- Smoke
- Sparks
- Burning smell
- Unexpected heating
- Unstable or implausible temperature readings
- Failed cooling fans
- Melted or discoloured connectors
- Repeated firmware safety errors
- Unexpected axis movement
- Severe mechanical noise or vibration

!!! warning "Do Not Ignore Warning Signs"
    An intermittent fault can still be dangerous.

    Stop the machine and identify the cause before returning it to normal operation.

---

## After Modifications

The My-Cloner is designed to be modified and developed.

Changes to hardware, wiring, heaters, sensors, fans, motion systems or Klipper configuration may affect previous validation.

After a significant modification:

1. Recheck the affected subsystem.
2. Repeat the relevant commissioning or validation steps.
3. Keep the printer under direct supervision during initial testing.
4. Return to normal operation only after the modified system behaves correctly.

Do not assume that a machine remains validated simply because it powers on or starts a print.

---

## Related Documentation

- [Wiring & Electronics](../wiring/index.md) — electrical architecture, controller connections and hardware assignments
- [Before First Power-On](../operation/initial-setup/before-first-power-on.md) — inspection before initial or renewed commissioning
- [First Power-On](../operation/initial-setup/first-power-on.md) — controlled staged power-up procedure