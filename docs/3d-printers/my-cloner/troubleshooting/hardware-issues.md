# Hardware Issues and Shutdowns

Klipper is designed with safety as a top priority. When it detects a problem that could be dangerous or damage the hardware, it enters a "shutdown" state. Understanding why it shut down is the key to fixing the problem.

!!! success "The Console is Your Best Friend"
    Unlike other firmwares that show cryptic codes, Klipper gives you a descriptive, human-readable error message in the **Console** tab of your web interface (Mainsail/Fluidd). **Always read the console output first!** After fixing the issue, you will need to click the `FIRMWARE_RESTART` button to clear the shutdown state.

<figure markdown="1">
  ![Hardware Issues](/images/image-placeholder.png#only-light){ width="600" }
  ![Hardware Issues](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration of various hardware components like power supply, motors, and sensors.</figcaption>
</figure>

---
### Temperature-Related Errors

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
### Homing and Endstop Errors

These errors typically occur when you try to home the printer.

* **Error Message:** `Endstop x still triggered after retract`
    * **Meaning:** The printer hit the endstop switch, moved away from it, but the firmware still sees the switch as being pressed.
    * **Causes:** A faulty mechanical endstop switch that is physically stuck, or incorrect wiring.
    * **Solution:** Check that your endstop switch can physically "click" and is not jammed. Check its wiring. If the pin name in your `printer.cfg` is prefixed with a `^` (pull-up), try removing it, or vice-versa.

* **Error Message:** `Homing failed to trigger endstop`
    * **Meaning:** The print head moved its full range of motion but never triggered the endstop switch.
    * **Causes:** The endstop is disconnected or its wire is broken; the switch itself is faulty; or there is a mechanical obstruction preventing the axis from reaching the endstop.
    * **Solution:** Check the endstop wiring. Manually press the switch and see if its status changes in the web interface. Check the axis for any physical obstructions.

---
### Configuration and Communication Errors

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