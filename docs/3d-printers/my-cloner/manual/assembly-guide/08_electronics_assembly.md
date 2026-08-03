# Electronics Assembly

Welcome to the final assembly chapter. Here we will mount the mainboard (MCU) into its protective case, connect all the cables from the motors and sensors, and perform the final cable management.

!!! danger "CRITICAL: Electrostatic Discharge (ESD) Warning"
    The mainboard is the brain of your printer and is highly sensitive to static electricity. A small shock can permanently damage it.
    * **Keep the mainboard in its anti-static bag** until the moment you are instructed to install it.
    * **Handle the board by its edges.** Never touch the chips, capacitors, or other components on its surface.
    * **Discharge yourself first.** Before handling the board, touch a large, grounded metal object (like a radiator or metal desk leg) to discharge any static electricity from your body.

---
### Step 1: Tools Necessary for This Chapter

* **Tools needed:**
    * Needle-nose pliers (for trimming zip ties)
    * Philips screwdriver (for power terminals)
    * 1.5mm and 2.5mm Allen keys

---
### Step 2: Preparing and Mounting the Electronics Case Door

First, we will assemble the hinged door for the electronics case. This combines several smaller preparation and assembly steps.

* **Parts needed:**
    * `Einsy-door` (1x printed part)
    * `Einsy-hinge-top` (1x printed part)
    * `Einsy-hinge-bottom` (1x printed part)
    * M3nS nut (1x)
    * M3x10 screw (2x)
* **Action:**
    1.  Take the `Einsy-door` and insert the M3nS nut all the way into its slot.
    2.  Identify the mounting holes on the printer's frame for the hinges.
    3.  Attach the `Einsy-hinge-bottom` to the lower mounting hole on the frame.
    4.  Place the `Einsy-door` onto the bottom hinge.
    5.  Place the `Einsy-hinge-top` onto the top of the door and secure it to the frame with the remaining screw. Check that the door can open and close freely.

---
### Step 3: Preparing the X-Axis Motor Cable

Before we mount the main case, let's prepare the X-axis motor cable for neat routing.

* **Parts needed:**
    * Textile sleeve (small diameter)
    * Zip tie (1x)
* **Action:** Wrap the small textile sleeve around the cable coming from the X-axis motor. The sleeve will not cover the entire length of the cable.
* **Action:** Use a zip tie to temporarily secure the end of the sleeve to the cable bundle.

---
### Step 4: Preparing the Mainboard Case

Now we will prepare the main housing that holds the printer's electronics. This combines several preparation steps.

* **Parts needed:**
    * `Einsy-base` (1x the main printed case)
    * Mainboard / MCU (1x)
    * Various M3 screws, M3n, and M3nS nuts.

!!! tip "Raspberry Pi Slot"
    The mainboard case may have a small, removable piece of plastic covering an opening. This opening is designed to give access to the GPIO pins for installing a Raspberry Pi Zero W directly onto the mainboard, which is a popular way to run Klipper. If you plan this upgrade, you can carefully cut this piece away now.

* **Action:** Take the `Einsy-base` printed part and insert all the required M3nS and M3n nuts into their designated hexagonal and square slots. Use an Allen key to ensure they are all properly aligned.
* **Action:** Carefully place the mainboard into the base and secure it with four M3x10 screws. Tighten the screws gently to avoid damaging the circuit board.

---
### Step 5: Mounting the Mainboard Case to the Frame

Now we will attach the case containing the mainboard to the printer's frame.

* **Action:** First, loosely insert two M3x10 screws into the designated mounting holes on the printer's Z-axis frame. Do not screw them all the way in.

!!! tip "Connect the X-Axis Motor Cable First!"
    It is much easier to connect the X-axis motor cable to the mainboard **before** you mount the case to the frame.
    * **Action:** Plug the X-axis motor cable (the one wrapped in a textile sleeve) into its port on the mainboard, labeled "X".
    * **Action:** Neatly push the sleeved part of the cable into its slot on the `Einsy-base` case.

* **Action:** Slide the mainboard case onto the two screws you prepared on the frame.
* **Action:** Align the case with the edge of the Z-axis frame and then fully tighten both screws to secure it.

<figure markdown="1">
  ![Mounting the Mainboard Case](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![Mounting the Mainboard Case](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing the mainboard case being slid onto the mounting screws on the frame.</figcaption>
</figure>

---
### Step 6: Routing and Bundling the Main Cables

This is a multi-part process to create one neat cable bundle that runs along the printer's frame to the electronics case.

!!! warning "Do Not Overtighten Zip Ties"
    Throughout this process, tighten the zip ties so they are snug and hold the wires securely, but do not overtighten them. Overtightening can cut into the wire insulation and cause electrical shorts.

1.  **Start on the Right Side:** Begin by taking the cable from the right-side Z-axis motor. Route it along the bottom extrusion and use a zip tie to secure it to the frame through the designated holes.
2.  **Add PSU Cables:** Take the bundle of cables coming from the Power Supply Unit (PSU). Route them along the bottom extrusion, add them to the bundle with the Z-motor cable, and secure them with a second zip tie. Ensure the cables are tucked below the path of the Y-axis smooth rods.
3.  **Add Y-Motor Cable:** Next, add the Y-axis motor cable to the bundle and secure it with a third zip tie as you move along the frame.
4.  **Manage LCD Cables:** Take the two flat ribbon cables from the LCD screen. Neatly tuck them into the channel of the vertical aluminum extrusion to hide them. Leave the ends hanging out at the top for now.
5.  **Cross Over and Continue:** Route the main cable bundle up the frame, passing *over* the tucked-in LCD cables. Secure the bundle with another zip tie.
6.  **Final Bundle:** Near the top, add the left-side Z-motor cable to the main bundle. Carefully bring the two LCD ribbon cables out from the extrusion channel and join them with the bundle as well. Secure everything together with the final zip ties on this side of the frame.

<figure markdown="1">
  ![Main Cable Bundle Routing](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Main Cable Bundle Routing](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>The final, neatly managed cable bundle running along the side of the printer frame.</figcaption>
</figure>

---
### Step 7: Finalizing the Frame Cable Bundle

This is the final step in tidying up the main cable bundle that runs along the printer's frame.

* **Action:** Gently tighten the last few zip ties around the cable bundle. Remember, the goal is to keep the wires neat and secure, not to crush them. Cut the remaining ends of the zip ties flush with your pliers.
* **Action:** You can now turn the printer back onto its feet.

---
### Step 8: Securing the Heatbed Cable Bundle

Now we will connect the cable bundle coming from the heated bed to the electronics case.

* **Parts needed:**
    * `Heatbed-cable-clip` (1x printed part)
    * M3x10 screw (2x)
* **Action:** Guide the heatbed's textile-sleeved cable bundle into its designated holder on the `Einsy-base`. Make sure the sleeve itself is inside the holder for proper strain relief.
* **Action:** Use the `Heatbed-cable-clip` and two M3x10 screws to firmly clamp the cable bundle in place. Pay attention to the orientation of the clip to ensure the electronics case door will be able to close later.

---
### Step 9: Connecting the High-Power Wires (PSU & Heatbed)

This is the most critical wiring step of the entire build. Please read all instructions carefully before proceeding. An error here can damage your electronics.

!!! danger "CRITICAL: Check Polarity and Orientation"
    * **Polarity is Everything:** You must connect the POSITIVE `(+)` wire to the POSITIVE `(+)` terminal and the NEGATIVE `(-)` wire to the NEGATIVE `(-)` terminal. The positive wire is typically marked with a **red line** or is entirely **red**. The negative wire is **black**.
    * **Connector Orientation:** The metal "fork" connectors on the wires have a slight bend. The bent part must always face **UP**, away from the circuit board.
    * **Tighten Firmly:** All screws on these green power terminals must be tightened firmly with a Philips screwdriver. A loose connection can cause overheating.

* **Connection Order:**
    1.  **PSU Cable 1:** Connect the first pair of wires from the PSU to the leftmost power terminal.
    2.  **PSU Cable 2:** Connect the second pair of wires from the PSU to the middle power terminal.
    3.  **Heatbed Cable:** Connect the pair of wires from the Heatbed to the rightmost power terminal.

<figure markdown="1">
  ![Main Power Wiring](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Main Power Wiring](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>The final, correct wiring for the PSU and Heatbed power cables on the mainboard.</figcaption>
</figure>

---
### Step 10: Installing the Power Terminal Cover

Once you have triple-checked your power connections, it's time to install the safety cover.

* **Parts needed:**
    * `PSU-cover` (1x printed part)
    * M3x10 screw (2x)
* **Action:** Do one final check that the polarity is correct and all screws are tight.
* **Action:** Slide the printed `PSU-cover` over the green power terminals and secure it with two M3x10 screws.

---
### Step 11: Securing the Extruder Cable Bundle

Finally, let's secure the main cable bundle coming from the extruder and hotend.

* **Action:** Guide the large, textile-sleeved cable bundle towards its holder on the `Einsy-base`.

!!! tip "Strain Relief is Key"
    Your electronics case has a small, dedicated hole for the thick nylon filament stiffener that is inside your cable bundle.
    * **Action:** Guide the end of the nylon filament into this hole. This provides excellent strain relief and prevents the cables from being pulled out of their connectors.

* **Action:** Once the nylon filament is seated, place the entire sleeve into its holder.
* **Action:** Use the `Extruder-cable-clip` and two M3x10 screws to firmly clamp the bundle in place.

---
### Step 12: Connecting the LCD and Motor Cables

Now we will begin connecting the main components to the electronics board.

* **LCD Cables:**
    !!! warning "Check LCD Cable Order"
        It is critical to plug the two flat ribbon cables from the LCD into the correct ports.
        * The cable with **ONE stripe** connects to the port labeled **EXP1**.
        * The cable with **TWO stripes** connects to the port labeled **EXP2**.

* **Motor Cables:**
    * **Action:** Plug in the cables for the Y-axis motor, both Z-axis motors, and the Extruder motor into their clearly labeled ports on the mainboard.
    * **Action:** Create small, neat loops with the excess cable length before plugging them in.

* **Power Panic Cable:**
    * **Action:** Guide the Power Panic cable to its port in the bottom right corner of the board and plug it in.

<figure markdown="1">
  ![Motor and LCD Connections](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Motor and LCD Connections](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Illustration showing the correct ports for the LCD and motor cables.</figcaption>
</figure>

---
### Step 13: Connecting the Extruder and Hotend Wires

This is the final, most dense wiring step. Take your time and connect each component one by one.

!!! danger "CRITICAL: Check Sensor Voltage Pins (3-pin connectors)"
    Some sensors (like the filament sensor) use 3-pin connectors that have 5V power. Plugging these into the wrong pins, even if they fit, can **instantly and permanently destroy the sensor**. Triple-check the alignment and refer to your board's diagram.

* **Action:** Following the labels on your mainboard, connect the remaining cables from the extruder's main bundle in the following order:
    1.  **IR Filament Sensor:** Connect to the dedicated 3-pin sensor port. Verify the orientation.
    2.  **Part Cooling Fan (`Print fan`):** Connect to its labeled fan port.
    3.  **Hotend Thermistor:** Connect to its labeled thermistor port.
    4.  **Z-Probe (`SuperPINDA`):** Connect to its dedicated probe port.
    5.  **Hotend Heater:** Connect the two thicker wires to the heater power terminal.
    6.  **Hotend Fan:** Connect to its labeled fan port.

* **Cable Management:** Use two zip ties inserted through the holes in the electronics case to neatly bundle all of these wires along the side of the case.

---
### Step 14: Final Verification

This is your last chance to check all connections before closing the case.

!!! success "Final Checkpoint: Verify Everything!"
    Take a moment and carefully compare your fully wired board to the reference diagram. Check the following:
    * Are all connectors fully seated in their ports?
    * Are the high-power wires (from the PSU and Heatbed) screwed in tightly?
    * Is the polarity `(+)` and `(-)` correct for all power connections?
    * Are the 3-pin sensor cables (Filament Sensor, Z-Probe) plugged into the correct ports with the correct orientation?

<figure markdown="1">
  ![Fully Wired Mainboard](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Fully Wired Mainboard](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>A diagram of the fully wired mainboard for final comparison.</figcaption>
</figure>

---
### Step 15: Finalizing the Electronics Case

Once you are confident that all wiring is correct, it's time to close up the case.

* **Parts needed:**
    * M3x40 screw (1x)
* **Action:** Carefully close the hinged `Einsy-door`, making sure that no wires are pinched between the door and the case.
* **Action:** Secure the door with the long M3x40 screw.

---
### Step 16: Mounting the Antivibration Feet

This is a final reminder in case you skipped this step earlier.

* **Action:** If you haven't already installed the four rubber anti-vibration feet into the ends of the aluminum extrusions, please do so now.

---
### Step 17: Assembling and Mounting the Spool Holder

The final mechanical part to assemble is the spool holder, which will sit on top of the printer's frame. This combines a few smaller steps.

* **Parts needed:**
    * The three printed parts of the double spool holder (`Centre part` and two `Side arms`).
* **Assembly:**
    1.  The arms connect to the center part using a twist-and-lock mechanism.
    2.  Insert one arm into the center part and rotate it about half a turn until it locks firmly in place. Do not use excessive force.
    3.  Repeat for the second arm on the other side.
* **Mounting:**
    * To mount the assembled spool holder onto the top of the printer frame, first hook the small "tooth" on the holder onto the center of the frame.
    * Then, press downwards and backwards firmly to snap the holder's C-shaped clips onto the frame.

<figure markdown="1">
  ![Mounting the Spool Holder](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![Mounting the Spool Holder](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing the "hook and press" motion to mount the spool holder onto the top frame.</figcaption>
</figure>

---
### Step 18: Attaching the Serial Number Label (Important)

Your kit may come with a silver label containing your printer's unique serial number. This is an important step for identifying your machine for any future support or warranty claims.

!!! info "Why is this important?"
    The serial number is the unique identity of your printer. Its presence may be necessary for any warranty claim.

* **Action:** If a label is not already affixed to the frame, locate the silver serial number label.
* **Action:** Clean a spot on the rear of the printer's frame (e.g., above the PSU) to remove any dirt or grease.
* **Action:** Carefully peel the label from its backing and apply it smoothly to the cleaned area, ensuring no air bubbles are trapped underneath.

---
### Step 19: The Build is Complete!

!!! success "Congratulations, You've Assembled Your 3D Printer!"
    You have just finished the complete mechanical and electrical assembly of your machine. This was a long and challenging process, and you've done a fantastic job!

    The final step before you can start printing is to perform the "Pre-Flight Check" and the initial software calibrations.

