# Step 12: Low Voltage & Signal Wiring

With the power systems in place, we can now connect all the motors, fans, and sensors to the controller board. Keep your board's pinout diagram handy.

### Step 1: Z-Axis Motors

Connect the four Z-axis motors to the first four motor driver sockets on your controller board (typically labeled M0, M1, M2, M3).

!!! tip "Stepper Wire Colors Are Not Standard"
    The color of the wires for stepper motors can vary between manufacturers. Do not assume the colors are correct. Consult the datasheet for your specific motors to identify the A and B coil pairs (e.g., A+, A-, B+, B-).

<figure markdown="1">
  ![Wiring the Z-axis motors](../../images/image-placeholder.png#only-light){ width="700" }
  ![Wiring the Z-axis motors](../../images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>Diagram showing the four Z-motor cables being plugged into the M0, M1, M2, and M3 driver outputs on the controller board.</figcaption>
</figure>

### Step 2: Bed and Frame-Mounted Components

Connect the components that are attached to the main frame and bed.

* **Bed Thermistor**: Connect the thermistor from the heated bed to the primary thermistor input on the board (often labeled TH0 or TB).
* **Z-Endstop**: Connect the Z-endstop microswitch to the Z- endstop input pins.

### Step 3: Toolhead and Gantry Wiring

This involves connecting the large bundle of wires coming from the main cable chain.

* **A/B Motors**: Connect the A and B motors to their respective driver sockets.
* **Extruder Motor**: Connect the extruder motor on the toolhead to the E0 driver socket.
* **Hotend Heater**: Connect the hotend heater cartridge wires to a heater output (e.g., HE0).
* **Hotend Thermistor**: Connect the hotend thermistor to its corresponding input (e.g., TH1).
* **Fans**: Connect the Part Cooling Fan and Hotend Cooling Fan to their designated fan outputs. Ensure the polarity (+ and -) is correct.
* **X/Y Endstops**: Connect the X and Y endstop switches to their respective inputs.
* **Inductive Probe**: Connect the power (VCC and GND) and signal wires for the inductive probe to the designated probe or endstop port.

<figure markdown="1">
  ![Wiring the toolhead components to the board](../../images/image-placeholder.png#only-light){ width="900" }
  ![Wiring the toolhead components to the board](../../images/image-placeholder.png#only-dark){ width="900" }
  <figcaption>A comprehensive diagram showing all the wires from the main harness (motors, heater, fans, probe, endstops) connecting to their correct ports on the controller board.</figcaption>
</figure>