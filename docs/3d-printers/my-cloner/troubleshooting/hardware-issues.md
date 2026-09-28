# Hardware Issues and Shutdowns

Klipper is designed with safety as a top priority. When it detects a problem that could be dangerous or damage the hardware, it enters a "shutdown" state. Understanding why it shut down is the key to fixing the problem.

!!! success "The Console is Your Best Friend"
    Unlike other firmwares that show cryptic codes, Klipper gives you a descriptive, human-readable error message in the **Console** tab of your web interface (Mainsail/Fluidd). **Always read the console output first!** After fixing the issue, you will need to click the `FIRMWARE_RESTART` button to clear the shutdown state.

<figure markdown="1">
  ![Hardware Issues](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Hardware Issues](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>Illustration of various hardware components like power supply, motors, and sensors.</figcaption>
</figure>

---
## Temperature-Related Errors

These are the most common critical errors and are related to your heaters and temperature sensors (thermistors).

* **Error Message:** `Heater extruder not heating at expected rate`
    * **Meaning:** This is Klipper's version of "Thermal Runaway" or "Preheat Failure." The firmware told the heater to turn on, but the thermistor didn't detect the expected temperature rise in time.
    * **Likely Causes:**
        1.  A faulty heater cartridge or a loose wire.
        2.  A thermistor that has fallen out of the heater block.
        3.  A poor PID tune, causing the temperature to rise too slowly.
        4.  A strong draft from a window or A/C unit cooling the hotend.
    * **Solution:** Check all wiring for the heater and thermistor. Ensure the thermistor is securely seated inside the heater block. Run a `PID_CALIBRATE` command for your hotend.

* **Error Message:** `Thermistor temperature XX is outside valid range`
    * **Meaning:** The thermistor is reporting a temperature that is outside the `min_temp` or `max_temp` defined in your `printer.cfg`. This is Klipper's version of "MINTEMP" or "MAXTEMP".
    * **Likely Causes:**
        * **For low temperatures (e.g., -15°C):** A disconnected thermistor or a broken wire.
        * **For high temperatures (e.g., 500°C):** A short circuit in the thermistor wiring.
    * **Solution:** With the power off, check the thermistor's connection on your mainboard and inspect the entire length of the wire for damage.

---
## Homing and Sensorless-Homing Errors

The My-Cloner Rev A uses **TMC2209 sensorless homing** on X and Y and a **P.I.N.D.A. probe** for Z.

Klipper may still use the word `endstop` in error messages because the TMC2209 DIAG signal is configured as a virtual endstop. This does **not** mean that the Rev A has physical X/Y endstop switches.

* **Error Message:** `Endstop x still triggered after retract` or a similar virtual-endstop error
    * **Meaning:** Klipper still sees the X sensorless-homing input as triggered when it expects the axis to be released.
    * **Likely Causes:**
        1. Incorrect TMC2209 DIAG configuration.
        2. StallGuard sensitivity is too high.
        3. Motor current is unsuitable for the homing test.
        4. The axis is mechanically binding.
        5. The DIAG signal or MCU pin assignment does not match the Rev A I/O map.
    * **Solution:** Confirm TMC2209 UART communication, check the X DIAG mapping (`PA15`), inspect free axis movement, and retune the sensorless-homing parameters conservatively.

* **Error Message:** `Homing failed to trigger endstop`
    * **Meaning:** The axis completed the allowed homing movement without the configured virtual endstop triggering.
    * **Likely Causes:**
        1. StallGuard sensitivity is too low.
        2. The DIAG pin is incorrect or not electrically connected as expected.
        3. TMC2209 UART/driver configuration is incorrect.
        4. The configured homing direction is wrong.
        5. Motor current or homing speed is unsuitable.
    * **Solution:** Stop repeated homing attempts. Confirm the board mapping and TMC2209 communication first, then tune `driver_SGTHRS`, motor current and homing speed in small controlled steps.

* **Z Homing / Probe Error**
    * **Meaning:** Klipper cannot obtain a valid Z reference from the P.I.N.D.A. probe.
    * **Likely Causes:** Incorrect probe input, wiring problem, probe mounting/height issue, or incorrect signal polarity.
    * **Solution:** Verify the P.I.N.D.A. input state before Z homing. Do not allow the nozzle to approach the bed if the probe state is not changing reliably.

!!! warning "Do Not Diagnose Rev A as a Mechanical-Endstop Printer"
    Do not troubleshoot X/Y by looking for a switch to press or click.

    The authoritative Rev A homing architecture is documented in [Motors & Homing](../wiring/motors-and-homing.md).

---
## Configuration and Communication Errors

These errors are often related to your `printer.cfg` file or the connection between the host and the MCU.

* **Error Message:** `Option '[option_name]' is not valid in section '[section_name]'`
    * **Meaning:** You have a typo in your `printer.cfg` file.
    * **Solution:** This is an easy fix! Klipper is telling you exactly where the error is. Open your `printer.cfg`, go to the specified section, and correct the spelling of the option based on the official Klipper documentation.

* **Error Message:** `MCU 'mcu' shutdown: Lost communication with MCU`
    * **Meaning:** The Raspberry Pi (host) lost its USB connection to the printer's mainboard (MCU).
    * **Solution:** This is a connectivity issue. Refer to the `Troubleshooting Klipper Connectivity Issues` guide. The most common causes are a bad USB cable or the MCU losing power.

* **Error Message:** `Must home axis first`
    * **Meaning:** You tried to perform a move that requires a known position (like a `G0` or `G1` move) before homing the printer with `G28`.
    * **Solution:** This is normal behavior. Always home the printer after turning it on or after a `FIRMWARE_RESTART` before you try to move any axes.
