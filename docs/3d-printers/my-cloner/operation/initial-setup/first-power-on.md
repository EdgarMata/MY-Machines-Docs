# First Power-On

This page describes the first controlled power-up of the **My-Cloner Rev A**.

Only continue if all checks in [Before First Power-On](before-first-power-on.md) have been completed successfully.

!!! warning "Do Not Continue If Any Check Failed"
    If any mechanical, electrical or wiring issue is still unresolved, disconnect the printer and correct it before powering on.

---

## 1. Prepare for Power-On

Before switching on the printer:

- Make sure the machine is on a stable surface.
- Keep your hands clear of all moving parts.
- Make sure no tools or loose objects are inside the printer.
- Keep the mains power switch accessible.
- Keep the printer connected only to the intended power source.

Do not start any homing, heating or movement commands yet.

---

## 2. Connect Mains Power

Connect the printer to the mains supply using the IEC power inlet.

Make sure the power switch is still in the OFF position before connecting the cable.

---

## 3. Switch On the Printer

Turn on the printer using the IEC power switch.

Immediately observe the machine.

Look and listen for anything unusual.

Normal signs may include:

- Power supply startup
- Mainboard LEDs
- Raspberry Pi activity LEDs
- Fans starting, depending on configuration

!!! danger "Switch Off Immediately If Necessary"
    Turn off the printer and disconnect mains power immediately if you notice:

    - Smoke
    - Sparks
    - Burning smell
    - Unusual heat
    - Repeated electrical clicking
    - Unexpected motor movement
    - Any component becoming hot without a command

Do not power the printer again until the cause has been identified.

---

## 4. Check the Power System

During the first power-up, verify that the electrical system behaves normally.

Check that:

- The Mean Well LRS-350-24 powers on normally.
- The MKS Robin Nano V3 receives power.
- The Raspberry Pi Zero 2 W starts correctly.
- No wiring or connector becomes warm.
- No fuse blows.
- No component shows visible signs of electrical stress.

If test equipment is available, confirm the power rails:

- Main system supply: approximately **24 V DC**
- Raspberry Pi supply: approximately **5 V DC**

!!! warning "Measure Safely"
    Take voltage measurements only if you are comfortable using a multimeter around powered electronics.

    Avoid shorting adjacent terminals with the meter probes.

---

## 5. Wait for the Raspberry Pi to Start

Allow the Raspberry Pi Zero 2 W to complete its startup process.

The boot process may take some time after power is applied.

Do not repeatedly switch the printer off and on during startup.

---

## 6. Connect to Mainsail

From a computer, tablet or phone connected to the same network, open the My-Cloner Mainsail interface.

When the interface loads, check the printer status.

The expected state is:

**Klipper Ready**

If Klipper reports an error, do not start moving or heating the printer until the error has been understood.

---

## 7. Check Temperature Readings

Before activating any heater, verify the temperature readings shown in Mainsail.

Check:

- Hotend temperature
- Heated bed temperature

At room temperature, both readings should be reasonably close to the ambient temperature.

They do not need to be exactly identical.

!!! danger "Invalid Temperature Reading"
    Do not activate a heater if:

    - A temperature sensor reports an impossible value
    - The reading is extremely high or low
    - The temperature changes suddenly without heating
    - Klipper reports a thermistor or ADC error

A faulty or incorrectly configured temperature sensor must be corrected before heater testing.

---

## 8. Check the Klipper MCU Connection

Confirm that Klipper can communicate with the **MKS Robin Nano V3**.

Mainsail should not display errors such as:

- MCU unable to connect
- Lost communication with MCU
- MCU shutdown

If the MCU does not connect, stop here and check the Klipper configuration, USB/serial connection and mainboard firmware.

---

## 9. Check the P.I.N.D.A. Probe Status

Verify that Klipper can read the P.I.N.D.A. probe state.

Do not perform Z homing yet.

The objective at this stage is only to confirm that the probe input responds correctly.

If the probe status does not change as expected, correct the issue before continuing.

---

## 10. Check the Filament Sensor

If the filament sensor is enabled in the current Klipper configuration, verify that its state can be detected correctly.

Insert and remove filament manually and confirm that the reported sensor state changes.

If the sensor is not yet enabled in Klipper, this check can be completed later during configuration.

---

## 11. Check Fans

Test the controllable fans individually from Mainsail or the Klipper console.

Confirm that:

- The part-cooling fan operates normally.
- The fan rotates in the correct direction.
- There are no unusual noises.
- The blades do not contact cables or printed parts.

The hotend fan may operate automatically depending on the Klipper configuration.

Do not continue if any fan is obstructed or wired incorrectly.

---

## 12. Do Not Home Yet

At this stage, do not perform automatic homing unless the X/Y sensorless-homing configuration, P.I.N.D.A. probe and axis directions have already been verified.

The next setup procedure will verify motion and homing in a controlled sequence.

---

## First Power-On Checklist

Before continuing, confirm the following:

- [ ] Printer powers on without smoke, sparks or abnormal smell.
- [ ] Mean Well LRS-350-24 operates normally.
- [ ] MKS Robin Nano V3 receives power.
- [ ] Raspberry Pi Zero 2 W starts normally.
- [ ] Klipper connects successfully to the MCU.
- [ ] Mainsail is accessible.
- [ ] Hotend temperature reading is plausible.
- [ ] Heated bed temperature reading is plausible.
- [ ] P.I.N.D.A. probe input responds correctly.
- [ ] Filament sensor responds correctly, if enabled.
- [ ] Fans operate correctly.
- [ ] No cable or connector becomes abnormally warm.
- [ ] No unexpected movement occurs.

---

!!! success "First Power-On Complete"
    If all checks above are successful, the electrical system is responding normally and the printer is ready for motion, homing and calibration checks.

Continue with:

[First Time Setup & Calibration](first-time-setup.md)