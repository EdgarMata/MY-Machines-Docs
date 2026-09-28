# Electrical and Thermal Safety

The **My-Cloner Rev A** combines **230 V AC mains wiring**, a **24 V DC power system** and components that operate at high temperature.

Treat electrical and thermal safety as part of normal operation, assembly and maintenance.

---

## Electrical Safety

!!! danger "230 V AC Mains"
    The AC input, IEC inlet and PSU mains terminals can expose hazardous voltage.

    Disconnect the printer from the power outlet before opening or modifying the electrical system.

Before operating the printer:

- Inspect mains and low-voltage wiring for damage.
- Confirm that protective earth is installed according to the approved electrical design.
- Confirm that high-current terminals are secure.
- Keep liquids away from the printer and electrical system.
- Do not operate the machine if a connector, cable or component shows signs of overheating.
- Stop using the printer if you notice smoke, sparks, burning smell or abnormal electrical noise.

Do not use the 24 V DC negative conductor as a substitute for protective earth.

---

## Hotend Safety

The Rev A hotend is designed for temperatures up to **300 °C**.

!!! danger "Burn Hazard"
    The nozzle and heater block can cause severe burns.

    Do not touch the hotend during heating, printing or cooldown.

Allow the hotend to cool to a safe temperature before maintenance.

The exact heater cartridge power and thermistor model must match the validated Rev A configuration.

---

## Heated-Bed Safety

The heated bed can remain hot for a significant time after heating is disabled.

Avoid touching the bed, spring-steel sheet or nearby hardware until the reported temperature has fallen to a safe level.

The final heated-bed operating limits are established during Rev A validation and must agree with the installed heater, thermistor and Klipper configuration.

---

## Temperature Monitoring

Klipper thermal protection depends on correct temperature-sensor configuration.

Before enabling a heater:

1. Confirm that the associated thermistor is connected.
2. Confirm that its reported temperature is plausible at room temperature.
3. Confirm that the configured `sensor_type` matches the installed hardware.
4. Confirm that the correct heater is associated with the correct sensor.
5. Stop immediately if temperature rises unexpectedly or the wrong component heats.

!!! danger "Never Bypass Thermal Protection"
    Do not disable Klipper temperature monitoring or heater-safety mechanisms to work around a wiring, sensor or configuration problem.

---

## Cooling

The 4010 hotend fan is part of the hotend thermal system.

Do not operate the hotend at extrusion temperatures without adequate heatsink cooling.

The My-Cloner Rev A uses **24 V fans**.

---

## Abnormal Behaviour

Disconnect the printer from mains power if you observe:

- Smoke
- Sparks
- Burning smell
- Unexpected heating
- A cable or terminal becoming abnormally hot
- Repeated electrical clicking
- A fan required for safe hotend operation stopping unexpectedly
- Uncontrolled motion that creates an immediate hazard

Investigate and correct the cause before powering the printer again.

---

## Related Documentation

For power-system details:

[Power Distribution](../wiring/power-distribution.md)

For heaters and temperature sensors:

[Heaters & Temperature Sensors](../wiring/heaters-and-temperature-sensors.md)

For cooling:

[Fans](../wiring/fans.md)

For the staged first-power procedure:

[Before First Power-On](../operation/initial-setup/before-first-power-on.md)
