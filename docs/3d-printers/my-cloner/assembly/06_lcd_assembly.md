# LCD Assembly

!!! warning "My-Cloner Rev A — Pending validation"
    This chapter retains legacy mechanical assembly references. Housing fit, fasteners and illustrations require confirmation against the Rev A CAD and installed hardware. Placeholder images are not wiring references. Follow the [Wiring & Electronics](../wiring/index.md) pages for Rev A assignments and complete [Before First Power-On](../operation/initial-setup/before-first-power-on.md) before energizing the machine.

Mainsail is the primary My-Cloner Rev A interface. The MKS TS35 V2.0 mounting and Klipper integration remain pending validation. The housing and control-knob steps below are legacy mechanical references and must not be assumed to fit the TS35.

---
## Step 1: Tools and Parts Preparation

First, let's gather all the parts needed for the LCD module. The bag with the small fasteners is often taped directly to the LCD screen itself.

* **Tools needed:**
    * 2.5mm Allen key
    * 2mm Allen key
* **Parts needed:**
    * LCD screen with controller board (1x)
    * `LCD-cover` (1x printed part)
    * `LCD-support` (2x printed parts)
    * `LCD-knob` (1x printed part)
    * M3x10 screw (6x)
    * M3nS nut (4x)
    * SD card (1x)

---
## Step 2: Checking the LCD Cables

!!! warning "TS35 Connection — Pending validation"
    Do not connect a display by cable stripes or assume EXP1/EXP2 compatibility. The TS35 connection method is TBD; use [Display & Filament Sensor](../wiring/display-and-filament-sensor.md).

<figure markdown="1">
  ![LCD Cable Check](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![LCD Cable Check](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing the back of the LCD with arrows pointing to the EXP1 and EXP2 ports and their corresponding cables.</figcaption>
</figure>

---
## Step 3: Assembling the LCD Housing

Now we will place the screen into its printed housing.

* **Action:** Take the two printed `LCD-support` parts and slide them onto the sides of the LCD controller board.
* **Action:** Carefully press this entire sub-assembly into the main `LCD-cover`. Be mindful of the control knob shaft on the other side. The controller should click securely into place.
* **Action:** Secure the LCD controller to the cover using two M3x10 screws from the back.

---
## Step 4: Mounting the LCD to the Frame

* **Action:** First, insert the four M3nS nuts into the prepared slots on the `LCD-support` parts that you just assembled.
* **Action:** Take the completed LCD assembly and place it against the front plate of the printer's main frame.

!!! warning "Check for Anti-Vibration Feet"
    If you haven't installed the printer's anti-vibration feet yet, the printer's frame might rest directly on the LCD housing, potentially damaging it. It is highly recommended to install the feet now if you haven't already.

* **Action:** Align the mounting holes and secure the LCD assembly to the frame using four M3x10 screws.

---
## Step 5: Assembling the Control Knob

* **Action:** Take the printed `LCD-knob` and press it firmly onto the metal shaft of the rotary encoder on the front of the screen.

---
## Step 6: LCD Assembly is Finished!

The LCD module is now fully assembled and mounted.

* **Action:** You can now carefully peel the protective film from the LCD screen.
* **Action:** You can also insert the included SD card into the slot on the left side of the screen.

!!! success "Ready for the Power Systems"
    Great job! With the user interface complete, we are ready to move on to the next chapter: assembling the heatbed and the power supply unit.