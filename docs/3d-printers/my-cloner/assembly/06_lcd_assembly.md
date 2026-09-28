# Display Assembly

In this chapter, we will mechanically assemble and mount the **MKS TS35 V2.0** display used by the My-Cloner Rev A.

**Mainsail is the primary user interface for the My-Cloner Rev A.** The TS35 is the local display hardware, but its final electrical and Klipper integration is still under validation.

---
### Step 1: Tools and Parts Preparation

First, let's gather all the parts needed for the display module. The bag with the small fasteners is often taped directly to the LCD screen itself.

* **Tools needed:**
    * 2.5mm Allen key
    * 2mm Allen key
* **Parts needed:**
    * MKS TS35 V2.0 display (1x)
    * `LCD-cover` (1x printed part)
    * `LCD-support` (2x printed parts)
    * `LCD-knob` (1x printed part)
    * M3x10 screw (6x)
    * M3nS nut (4x)
    * SD card (1x)

---
### Step 2: Checking the Display Cables

!!! warning "Electrical Integration Pending"
    The Robin Nano V3 exposes EXP1 and EXP2 headers, but the final MKS TS35 V2.0 connection method and operating mode under Klipper are still being validated.

    Do not connect ribbon cables solely from stripe count or from inherited printer instructions.

    Before electrical connection, follow the current [Display & Filament Sensor](../wiring/display-and-filament-sensor.md) documentation and the validated Rev A wiring schematic.

<figure markdown="1">
  ![LCD Cable Check](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![LCD Cable Check](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing the back of the LCD with arrows pointing to the EXP1 and EXP2 ports and their corresponding cables.</figcaption>
</figure>

---
### Step 3: Assembling the LCD Housing

Now we will place the screen into its printed housing.

* **Action:** Take the two printed `LCD-support` parts and slide them onto the sides of the display controller board.
* **Action:** Carefully press this entire sub-assembly into the main `LCD-cover`. Be mindful of the control knob shaft on the other side. The controller should click securely into place.
* **Action:** Secure the display controller to the cover using two M3x10 screws from the back.

---
### Step 4: Mounting the LCD to the Frame

* **Action:** First, insert the four M3nS nuts into the prepared slots on the `LCD-support` parts that you just assembled.
* **Action:** Take the completed LCD assembly and place it against the front plate of the printer's main frame.

!!! warning "Check for Anti-Vibration Feet"
    If you haven't installed the printer's anti-vibration feet yet, the printer's frame might rest directly on the LCD housing, potentially damaging it. It is highly recommended to install the feet now if you haven't already.

* **Action:** Align the mounting holes and secure the LCD assembly to the frame using four M3x10 screws.

---
### Step 5: Assembling the Control Knob

* **Action:** Take the printed `LCD-knob` and press it firmly onto the metal shaft of the rotary encoder on the front of the screen.

---
### Step 6: Display Mechanical Assembly is Finished!

The display module is now fully assembled and mounted.

* **Action:** You can now carefully peel the protective film from the LCD screen.
* **Action:** You can also insert the included SD card into the slot on the left side of the screen.

!!! success "Ready for the Power Systems"
    Great job! With the user interface complete, we are ready to move on to the next chapter: assembling the heatbed and the power supply unit.