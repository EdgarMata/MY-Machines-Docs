# Heatbed & PSU Assembly

!!! warning "My-Cloner Rev A — Pending validation"
    This chapter retains legacy mechanical assembly references. Housing fit, fasteners and illustrations require confirmation against the Rev A CAD and installed hardware. Placeholder images are not wiring references. Follow the [Wiring & Electronics](../wiring/index.md) pages for Rev A assignments and complete [Before First Power-On](../operation/initial-setup/before-first-power-on.md) before energizing the machine.

In this chapter, we will prepare and mount the two main power components of the printer: the Heatbed, where your prints will be built, and the Power Supply Unit (PSU), which provides all the energy for the machine.

!!! warning "Pay Close Attention to Wiring"
    This chapter involves connecting high-power electrical components. Please follow the instructions for polarity and wiring precisely to avoid damaging your printer or creating a safety hazard.

---
## Heatbed Wiring

First, we will securely attach the main power cable to the heated bed.

### Step 1: Preparing the Heatbed Power Cable

Gather all the necessary components for this crucial connection.

* **Parts needed:**
    * Heatbed (1x)
    * Heatbed power cable (1x, with red and black wires)
    * M3x10 screw (2x)
    * M3 washer (2x)
    * M3nN nyloc nut (2x)

### Step 2: Attaching the Power Cable

!!! danger "CRITICAL: Check Wire Polarity"
    Connecting the wires with the wrong polarity will damage your printer's electronics. Double-check every connection.
    * The **BLACK** wire **must** connect to the terminal labeled **GND**.
    * The **RED** wire **must** connect to the terminal labeled **VCC**.

* **Action:**
    1.  Place the ring terminal of the **black wire** over the heatbed pad labeled "GND".
    2.  Place a washer on top of the ring terminal.
    3.  Insert an M3x10 screw through the washer and the ring terminal into the heatbed.
    4.  On the other side of the heatbed, secure it with an M3nN nyloc nut. Use pliers and an Allen key to tighten it firmly.
    5.  Repeat this exact process for the **red wire**, connecting it to the pad labeled "VCC".

* **Final Adjustment:** Before the final tightening, gently bend the two metal ring terminals so they are angled slightly towards each other. This will help them fit inside the cable cover. Now, tighten both screws firmly.

<figure markdown="1">
  ![Heatbed Wiring Polarity](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![Heatbed Wiring Polarity](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing the correct polarity: the black wire connected to GND and the red wire to VCC.</figcaption>
</figure>

---
## Heatbed Cable Cover

Now we will install the printed cover that protects the solder joints and manages the cable strain.

### Step 3: Preparing the Cable Cover Parts

* **Parts needed:**
    * `Heatbed-cable-cover` (1x, the larger printed part)
    * `Heatbed-cable-cover-clip` (1x, the smaller printed part)
    * Textile sleeve (1x)
    * Various M3 screws and nuts.
* **Action:** Take the smaller `Heatbed-cable-cover-clip` and insert two M3n nuts into its slots.

### Step 4: Mounting the Main Cable Cover

* **Action:** Place the larger `Heatbed-cable-cover` onto the heatbed, aligning its hole with the central mounting hole on the bed's power terminal section. Secure it with an M3x10 screw and an M3nN nyloc nut.

!!! tip "Proper Thermistor Cable Management"
    The thin black cable already attached to the bed is the thermistor, which measures the bed's temperature.
    * **Action:** Ensure there is some slack in this cable underneath the cover. If it's too tight, it could break when the bed moves.
    * **Action:** To keep it neat, wrap the thermistor cable a few times around the main power cable bundle.

### Step 5: Wrapping and Securing the Cable Sleeve

* **Action:** Take the textile sleeve and begin wrapping it around the power and thermistor cables, starting from right behind the cable cover. Slide the first few centimeters of the sleeve inside the cover.
* **Action:** Take the smaller `Heatbed-cable-cover-clip` that you prepared earlier and place it on top of the main cover.

!!! warning "Do Not Pinch the Thermistor Wire!"
    The clip has a small channel or cutout specifically for the thermistor wire. Make sure the wire is seated neatly in this channel before you tighten the screws. Pinching this wire will damage it.

* **Action:** Secure the clip with two M3x10 screws, tightening them evenly. This will clamp the textile sleeve and wires firmly in place.

<figure markdown="1">
  ![Assembled Heatbed Cable Cover](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Assembled Heatbed Cable Cover](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>The final assembled heatbed cable cover, with the textile sleeve and wires securely clamped.</figcaption>
</figure>

---
## Heatbed Installation

### Step 6: Finalizing the Cable Wrap

* **Action:** Continue wrapping the textile sleeve neatly around the entire length of the heatbed cable bundle. When finished, you can twist the sleeve slightly to make it tighter and more uniform.

---
## Step 7: Mounting the Heatbed

Now we will mount the prepared heatbed assembly onto the Y-carriage.

* **Parts needed:**
    * M3x12b screw (9x)
    * 6x6x3t spacer (9x)
* **Action:**
    1.  Push the Y-carriage to the front of the printer. Place the heatbed on top of it.
    2.  Start with the **center hole**. Place one spacer on the center hole of the Y-carriage. Align the center hole of the heatbed with it and insert one screw. Do not tighten it fully yet.
    3.  Using pliers, carefully place the other eight spacers on their corresponding holes on the Y-carriage, between the carriage and the heatbed.
    4.  Insert the remaining eight screws into their holes.

!!! tip "Correct Tightening Sequence for a Flat Bed"
    To ensure the bed is mounted flat and without stress, tighten the nine screws in a specific order:
    1.  Tighten the **center screw** first.
    2.  Tighten the **four screws on the main edges** (front, back, left, right).
    3.  Finally, tighten the **four corner screws**.

<figure markdown="1">
  ![Heatbed Spacer Placement](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![Heatbed Spacer Placement](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing the placement of the spacers between the Y-carriage and the heatbed.</figcaption>
</figure>

---
## PSU Installation and Wiring

### Step 8: Preparing the PSU Parts

It's time to prepare the Power Supply Unit (PSU), the component that powers the entire printer.

* **Parts needed:**
    * Mean Well LRS-350-24 power supply (1x)
    * Required 24 V DC power cables
    * M4x10r screw (2x)
    * M3x10 screw (2x)

!!! warning "Input Voltage Selector"
    The Mean Well LRS-350-24 uses a selectable AC input range.

    For the standard My-Cloner Rev A configuration, verify that the selector is set correctly for **230 V AC** before connecting mains power.

---
## Step 9: Mounting the PSU to the Frame

* **Action:** Turn the printer so the rear side is facing you. Loosely screw two M3x10 screws into the printed PSU holders on the bottom extrusion.
* **Action:** Slide the PSU onto these screws. You may need to adjust the spacing of the holders so they align with the mounting holes on the side of the PSU.
* **Action:** Now, align the mounting holes on the front of the PSU with the corresponding holes on the printer's vertical frame. Insert and tighten the two M4 screws.
* **Action:** Before the final tightening, ensure the PSU is pressed firmly against both the bottom extrusion and the vertical frame. Once everything is aligned, fully tighten all the mounting screws (both the M3 and M4 screws).

---
### Step 10: Verify the PSU Electrical Connections

!!! danger "Mains Voltage"
    Do not make or modify AC mains connections while the printer is connected to the power outlet.

    The Mean Well LRS-350-24 includes dedicated AC input terminals and 24 V DC output terminals. Their exact functions must be identified from the markings on the installed PSU and the current My-Cloner electrical schematic.

Before connecting any conductor:

1. Verify the PSU model is **Mean Well LRS-350-24**.
2. Verify the input-voltage selector is set for the intended **230 V AC** supply.
3. Identify the AC **L**, **N** and protective-earth terminals.
4. Identify the 24 V DC positive and negative output terminals.
5. Check every cable destination against the current [Power Distribution](../wiring/power-distribution.md) page and the QElectroTech schematic.
6. Do not rely on terminal order copied from an older printer or PSU.

!!! important "Protective Earth"
    Protective earth is a safety connection and must be installed according to the approved Rev A electrical design.

---

### Step 11: Connect the 24 V DC Distribution

The PSU provides the main 24 V DC rail for the My-Cloner Rev A.

The 24 V distribution supplies:

- MKS Robin Nano V3
- Heater outputs
- Stepper drivers and motors
- 24 V cooling fans
- LM2596 converter input

Use correctly sized conductors and secure terminations. Verify polarity with a multimeter before connecting sensitive electronics.

The detailed distribution architecture and current validation status are maintained in:

[Power Distribution](../wiring/power-distribution.md)

---

### Step 12: Power-Loss Recovery

**Power Panic is not implemented in the My-Cloner Rev A.**

Do not install a Power Panic cable or assume that a legacy power-loss-recovery board is part of the current electrical architecture.

Any future power-loss-recovery feature must be documented as a separate validated revision before it is added to the assembly procedure.

---

### Step 13: Heatbed and PSU are Finished!

The main power systems of your printer are now fully assembled and mounted.

* **Action:** Take a final look at your assembly and compare it to the reference pictures. Ensure all screws are tight and all cables are routed neatly.

!!! note "Do Not Place the Steel Sheet on the Heatbed Yet"
    You will be instructed to place the flexible steel sheet on the heatbed during the initial calibration wizard after the assembly is complete. Leave it off for now.

!!! success "On to the Final Chapter!"
    Excellent work! With the power systems in place, you are ready for the final assembly chapter: connecting all the electronics.
