# Loading and Unloading Filament

This guide explains how to load and unload filament on the **My-Cloner Rev A**.

The My-Cloner uses a direct-drive extruder and an MK3-style IR filament sensor.

!!! warning "Heat the Hotend First"
    Never force filament through a cold hotend.

    The nozzle must be heated to a suitable temperature before loading or unloading filament.

---

## Before You Start

Make sure:

- The printer is powered on.
- Klipper is connected and ready.
- Mainsail is accessible.
- The hotend temperature reading is normal.
- The filament path is clear.
- The spool can rotate freely.

---

## Preparing the Filament

Before inserting filament:

1. Remove any damaged or deformed section from the filament end.
2. Cut the filament at approximately a 45° angle.
3. Make sure the tip is clean and straight.

A clean angled tip makes it easier to guide the filament through the extruder.

---

## Loading Filament

### 1. Heat the Hotend

Set the hotend to a suitable loading temperature for the filament.

Typical examples:

| Material | Typical Loading Temperature |
|---|---|
| PLA | 200–215 °C |
| PETG | 230–245 °C |
| ABS / ASA | 240–255 °C |

These values are general starting points.

Always follow the filament manufacturer's recommended temperature range.

---

### 2. Insert the Filament

Guide the filament into the extruder input.

Push it gently until it reaches the drive gears.

Do not force the filament if you feel unusual resistance.

Check that:

- The filament enters straight.
- The spool rotates freely.
- The filament does not catch on the sensor mechanism.

---

### 3. Feed the Filament

Once the hotend reaches the target temperature, use the extruder controls in Mainsail.

Extrude a small amount of filament at a time.

Continue until material starts flowing from the nozzle.

---

### 4. Purge the Nozzle

Continue extruding until:

- Filament flows continuously.
- The extrusion looks smooth.
- Any previous material or colour has been removed.

A short purge helps make sure the nozzle is fully loaded before printing.

---

## Verify the Filament Sensor

If the filament sensor is enabled in Klipper, confirm that it detects the inserted filament.

The reported state should change when filament is:

- Inserted
- Removed

If the sensor does not respond correctly, do not rely on filament runout detection until the sensor has been adjusted or configured.

---

## Unloading Filament

### 1. Heat the Hotend

Heat the nozzle to the normal printing temperature for the loaded material.

Do not attempt to pull cold filament from the hotend.

---

### 2. Retract the Filament

Use the Mainsail extruder controls to retract the filament.

Retract enough filament to release it from the hotend and extruder path.

---

### 3. Remove the Filament

Gently pull the filament out of the extruder.

Do not use excessive force.

If the filament does not release:

- Make sure the hotend is hot enough.
- Extrude a small amount first.
- Try retracting again.

---

## Changing Filament

When changing from one filament to another:

1. Heat the hotend for the currently loaded material.
2. Unload the old filament.
3. Prepare the new filament.
4. Insert the new filament.
5. Extrude until the new material flows cleanly from the nozzle.

When changing colours or materials, purge enough filament to remove the previous material from the hotend.

---

## Filament Storage

For reliable printing, keep filament clean and dry.

Recommended practices:

- Store filament in a dry location.
- Keep unused spools in sealed bags or containers.
- Use desiccant where appropriate.
- Keep dust and debris away from the filament path.

Moist filament can cause:

- Poor surface finish
- Stringing
- Popping sounds
- Inconsistent extrusion
- Weak prints

---

## If Filament Does Not Feed

If the extruder motor turns but filament does not move, check:

- Hotend temperature
- Filament path
- Drive gear tension
- Drive gear cleanliness
- Nozzle blockage
- Filament deformation
- Spool movement

Do not increase extruder force without identifying the cause.

---

## If Filament Is Stuck

If filament cannot be removed:

1. Heat the hotend to the correct temperature.
2. Extrude a small amount.
3. Retract the filament again.
4. Gently pull it from the extruder.

If the filament remains stuck, refer to the troubleshooting and maintenance documentation before disassembling the hotend.

---

!!! success "Filament Ready"
    Once filament flows smoothly from the nozzle and the filament sensor reports the correct state, the printer is ready for extrusion and printing tests.

For normal printer control, see:

[Klipper Interface Guide](klipper-interface-guide.md)