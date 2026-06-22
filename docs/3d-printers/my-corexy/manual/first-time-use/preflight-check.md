# Pre-flight Check

Before we command the printer to move, we must verify that all heaters, fans, and endstops are wired correctly and responding as expected. This "pre-flight check" prevents crashes and potential damage.

### Step 1: Check Thermistors

Look at the temperature readings in your web interface. Both the hotend and heated bed should be reporting a plausible ambient room temperature (e.g., 20-30°C).

!!! danger "Fix Thermistor Errors Now"
    If a temperature reads `0`, `-50`, or a very high number like `3000`, it indicates a wiring short or a broken wire. **You must fix this before proceeding.** Attempting to heat a component with a faulty thermistor is a major fire hazard.

### Step 2: Check Heaters

We will test each heater individually at a low temperature.

1.  **Hotend Heater**: In your web interface, set the hotend target temperature to 50°C. Watch the temperature graph to confirm that the temperature rises smoothly and stabilizes near 50°C. Once confirmed, turn the heater off.
2.  **Bed Heater**: Set the heated bed target temperature to 40°C. As before, watch the graph to confirm the temperature rises correctly, then turn it off.

<figure markdown="1">
  ![Temperature graph showing heater test](/images/image-placeholder.png#only-light){ width="700" }
  ![Temperature graph showing heater test](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>The temperature graph in the web interface showing a smooth curve as a heater correctly warms up to its target temperature.</figcaption>
</figure>

### Step 3: Check Fans

From your web interface, turn on each fan one at a time and visually confirm that it spins.
* Part Cooling Fan
* Hotend Cooling Fan
* Electronics Bay Fan(s)

### Step 4: Check Endstops

This is the most important check before homing. We will manually trigger each endstop and check its status in Klipper.

1.  Open the "Console" tab in your web interface.
2.  Type the command `QUERY_ENDSTOPS` and press Enter. It should report the status of all endstops as `open`.
3.  With your finger, gently press and hold the **X-axis** microswitch. While holding it, run `QUERY_ENDSTOPS` again. The output should now show `x: triggered`.
4.  Release the switch and repeat the process for the **Y-axis** and **Z-axis** endstops, confirming each one reports `triggered` only when pressed.

<figure markdown="1">
  ![Console output from QUERY_ENDSTOPS command](/images/image-placeholder.png#only-light){ width="800" }
  ![Console output from QUERY_ENDSTOPS command](/images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>The console in the web interface showing the output of the QUERY_ENDSTOPS command, both before and after an endstop is manually triggered.</figcaption>
</figure>

Once all heaters, fans, and endstops have passed these checks, your printer is ready for its first movements.
