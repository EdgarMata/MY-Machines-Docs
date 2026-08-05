# E-Axis (Extruder) Assembly

Welcome to the heart of your 3D printer: the E-axis, or Extruder. This complex assembly is responsible for gripping, melting, and pushing the filament through the nozzle with precision.

!!! warning "Please Read These Tips Before You Start"
    * **Take Your Time:** This is the most complex chapter of the build. Do not rush. A properly assembled extruder is essential for high-quality prints.
    * **Check Screw Lengths:** This chapter uses many M3 screws of different lengths (e.g., M3x10, M3x18, M3x20, M3x40). Pay close attention to the instructions to ensure you are using the correct screw in each step.
    * **Handle Magnets Carefully:** This assembly uses strong magnets. Keep them separated to prevent them from snapping together and breaking.
    * **Cable Management is Key:** Follow the cable routing instructions precisely. A pinched wire can be very difficult to fix later without disassembling the entire extruder.

---
### Step 1: Tools Necessary for This Chapter
* **Tools needed:**
    * Needle-nose pliers
    * 2.5mm Allen key
    * 2mm Allen key
    * 1.5mm Allen key

---
### Step 2: Preparing the Extruder Body Parts
Let's begin by gathering the main printed parts and the necessary hardware. This combines the first few parts-gathering steps of the reference manual.

* **Parts needed:**
    * `Extruder-body` (1x printed part)
    * `Adapter-printer` (1x printed part)
    * `FS-lever` (Filament Sensor Lever) (1x printed part)
    * Various M3 screws, M3n, and M3nS nuts
    * Steel ball (1x)
    * Magnet 10x6x2mm (1x, the smaller one)
    * Magnet 20x6x2mm (1x, the larger one)

---
### Step 3: Assembling the Extruder Body
In this step, we will insert the nuts and one of the magnets into the main body parts.

* **Action:** Take the `Extruder-body` printed part and insert the various M3n and M3nS nuts into their respective hexagonal slots. Use the "screw pulling technique" if a nut is too tight to press in by hand.
* **Action:** Take the `FS-lever` part and carefully insert the **smaller magnet** (10x6x2mm) into its designated slot.

---
### Step 4: Assembling the Filament Sensor Lever
This step is critical for the filament sensor to work correctly.

* **Action:** Insert the `FS-lever` (with its magnet) into the `Extruder-body`. Secure it with an M3x18 screw. The lever must be able to move freely after the screw is tightened.
* **Action:** Now, insert the **larger magnet** (20x6x2mm) into its slot in the `Extruder-body`.

!!! danger "CRITICAL: Magnet Polarity"
    The two magnets (one in the lever, one in the body) **must repel each other**. When correctly installed, the magnets will push the lever to the side. If they attract each other and the lever is pulled inwards, you have installed one of the magnets incorrectly. Flip one of them over and try again. An incorrect installation will cause the filament sensor to fail.

<figure markdown="1">
  ![Correct Magnet Repulsion](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Correct Magnet Repulsion](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Illustration comparing the correct lever position (pushed out by repelling magnets) vs. the incorrect position (pulled in by attracting magnets).</figcaption>
</figure>

---
### Step 5: Assembling the Steel Ball Mechanism
This mechanism helps guide the filament smoothly.

* **Action:** Take the `Adapter-printer` part and insert the steel ball into its socket. Roll the ball around to ensure it moves smoothly.
* **Action:** Place this `Adapter-printer` sub-assembly into the main `Extruder-body`. It should fit snugly into a groove. Do not use a screw to secure it yet.

---
### Step 6: Preparing the Extruder Motor and Gears
Now let's prepare the motor and the famous Bondtech gears that grip the filament.

* **Parts needed:**
    * Extruder motor (1x)
    * `Extruder-motor-plate` (1x printed part)
    * Bondtech drive gear (the one **with** a small grub screw)
    * Bondtech idler gear (the one **without** a grub screw - keep this and its bearings safe for a later step)
    * M3x10 screws (2x)

---
### Step 7: Assembling the Bondtech Drive Gear
* **Action:** Attach the `Extruder-motor-plate` to the extruder motor using two M3x10 screws. Use the motor's cable as a guide for the correct orientation.
* **Action:** Rotate the motor's shaft so the flat part is facing outwards.
* **Action:** Slide the Bondtech drive gear (the one with the grub screw) onto the shaft. The grub screw must be facing the flat part of the shaft. Tighten the screw slightly for now.

---
### Step 8: Aligning the Bondtech Drive Gear
This alignment is crucial to prevent filament grinding.

!!! tip "Use a Piece of Filament for Alignment"
    * **Action:** Take a straight piece of 1.75mm filament and place it along the filament path in the extruder body.
    * **Action:** Adjust the position of the Bondtech gear on the motor shaft up or down until its grooved teeth are perfectly aligned with the filament path.
    * **Action:** Once you are satisfied with the alignment, firmly tighten the grub screw against the flat part of the motor shaft. Be careful not to strip the small screw.

<figure markdown="1">
  ![Bondtech Gear Alignment](/assets/images/image-placeholder.webp#only-light){ width="400" }
  ![Bondtech Gear Alignment](/assets/images/image-placeholder.webp#only-dark){ width="400" }
  <figcaption>Illustration showing a piece of filament being used to align the groove in the drive gear with the filament path.</figcaption>
</figure>

---
### Step 9: Preparing the Extruder Cover

This is a quick preparatory step for the part that will close up the main extruder assembly.

* **Parts needed:**
    * `Extruder-cover` (1x printed part)
    * M3nS nut (1x)
* **Action:** Take the `Extruder-cover` and insert the M3nS square nut all the way into its slot. Use an Allen key to ensure it is properly aligned.

---
### Step 10: Joining the Main Extruder Body

This is a major step where we will join the two halves of the extruder into a single "sandwich."

* **Parts needed:**
    * The previously assembled Extruder-body
    * The previously assembled Extruder-motor
    * The prepared Extruder-cover
    * The Hotend assembly
    * M3x40 screw (2x)
* **Action:** Place the Hotend into the main `Extruder-body`, fitting it into the grooves designed for it. The heater block and nozzle should point downwards.
* **Pro-Tip:** To make assembly easier and protect the hotend wires, rest the `Extruder-body` on the edge of a small box.
* **Action:** Carefully place the Extruder-motor assembly onto the `Extruder-body`. Make sure the parts are aligned and the gears do not dislodge the magnet on the `FS-lever`.
* **Action:** Place the `Extruder-cover` on the other side.
* **Action:** Insert the two long M3x40 screws through all three parts and tighten them to secure the entire assembly.

---
### Step 11: Preparing the X-Carriage

Now we will prepare the `X-carriage`, which is the printed part that will mount this entire extruder assembly onto the X-axis rods.

* **Parts needed:**
    * `X-carriage` (1x printed part)
    * M3n nut (2x)
    * M3nS nut (4x)
    * IR-sensor cable (1x)
* **Action:** Insert all the nuts into their respective hexagonal and square slots on the `X-carriage`. Use the "screw pulling technique" for the round M3n nuts to seat them fully.
* **Action:** Take the IR-sensor cable and route it through the designated channel in the `X-carriage`. Leave a small amount of slack with the connector as shown in the reference images.

---
### Step 12: Attaching the X-Carriage to the Extruder

In this step, we will mount the prepared `X-carriage` to the back of the main extruder assembly. This step requires careful cable management.

!!! danger "CRITICAL: Check for Pinched Wires"
    Before and during tightening, constantly check that no wires are being pinched between the plastic parts. A pinched wire can lead to electrical shorts or component failure.

* **Action:** First, guide the extruder motor cable into its channel along the extruder body.
* **Action:** Place the `X-carriage` onto the back of the extruder assembly. The motor cable and the IR-sensor cable should both run neatly within the channels of the `X-carriage`.
* **Action:** Secure the two parts together using two M3x10 screws. **Do not fully tighten the screws yet**, as we still need to adjust the sensor cable length.

<figure markdown="1">
  ![Attaching X-Carriage](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Attaching X-Carriage](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Illustration showing the X-carriage being mounted to the rear of the extruder assembly, with careful cable routing.</figcaption>
</figure>

---
### Step 13: Assembling the IR Filament Sensor

Now we will install the sensor that detects the presence of filament.

* **Parts needed:**
    * IR-sensor PCB (1x)
    * M2x8 screw (1x)
    * M3x40 screw (1x)

!!! warning "Handle Electronics with Care"
    Hold the IR-sensor PCB by its edges. Avoid touching any of the chips or components on its surface to prevent damage from static electricity.

* **Action:** Place the IR-sensor on top of the `Extruder-body` and secure it with the small M2x8 screw. The "U-shaped" sensor component should be facing down.
* **Action:** Connect the IR-sensor cable (which you previously routed through the `X-carriage`). **Pay close attention to the correct orientation of the connector.**
* **Action:** Adjust the cable slack behind the sensor to create a small, neat loop.
* **Action:** Once the cable is connected and adjusted, you can now **fully tighten the two M3x10 screws** from the previous step.
* **Action:** Finish the sensor assembly by inserting the long M3x40 screw from the top, which passes through the `Extruder-cover` and secures it to the `X-carriage`.

---
### Step 14: Preparing to Mount the Hotend Fan

The hotend fan is critical for preventing "heat creep" and ensuring reliable extrusion. It constantly cools the heatsink to keep the filament solid until it reaches the melt zone.

!!! info "Check Your Fan Version"
    Your kit may come with different versions of the hotend fan. The primary difference is often in the cabling (e.g., one version may have a black protective sleeve, another may have loose colored wires) and the length of the mounting screws. The following instructions are for the version with a **black sleeve on its cable bundle**.

---
### Step 15: Preparing the Hotend Fan (Version A)

Let's gather the parts for this specific fan version.

* **Parts needed:**
    * Hotend fan (1x)
    * M3x14 screw (3x)

---
### Step 16: Assembling the Hotend Fan

This step involves careful cable management to ensure nothing gets pinched or restricts movement.

* **Fan Orientation:** The fan has two sides. The side with the manufacturer's **sticker must face inwards**, towards the extruder body. This ensures it blows air in the correct direction.
* **Cable Routing:**
    1.  Before mounting, create a small loop with the fan's cable near the fan's body.
    2.  Place the fan onto the extruder body and guide the cable into the **upper channel** of the extruder.
    3.  Gently push the fan towards the X-carriage, feeding the cable along the channel as you go.
    4.  Route the end of the cable into the main channel on the `X-carriage`, alongside the other cables you have already placed there.

!!! danger "Final Check: Do Not Pinch the Cable!"
    Before securing the fan, double-check the entire path of the cable. Make sure it is neatly tucked into its channels and is not being pinched between any plastic parts. A damaged fan cable will cause extrusion problems.

<figure markdown="1">
  ![Hotend Fan Cable Routing](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Hotend Fan Cable Routing](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Illustration showing the correct path for the hotend fan cable through the extruder body and into the X-carriage channel.</figcaption>
</figure>

---
### Step 17: Securing the Hotend Fan

Now, let's fasten the fan in place.

* **Action:** Use the three M3x14 screws to mount the fan to the extruder body.
* **Pro-Tip:** The screws are "self-tapping," meaning they create their own threads in the printed part. Tighten them until they are snug, but **do not overtighten**, as you can crack the fan's plastic casing.
* **Note:** One of the four screw holes on the fan will be left empty for now. It will be used in a later step.

---
### Step 18: Preparing the Extruder Idler Assembly

Now we will build the idler door, which works together with the motor's drive gear to grip and push the filament.

* **Parts needed:**
    * `Extruder-idler` (1x printed part, also known as the idler door)
    * Bondtech idler gear (the one **without** a grub screw)
    * Small bearings for the idler gear (2x)
    * Shaft for the idler gear (1x)
    * M3n nut (1x)
    * M3x40 screw (2x)
    * Idler spring (1x)

---
### Step 19: Assembling the Idler Gear and Door

Let's assemble the moving parts of the idler mechanism.

* **Action:** First, take the Bondtech idler gear and press the two small bearings into its center, one from each side.
* **Action:** Next, take the `Extruder-idler` printed part and insert the M3n nut into its hexagonal slot. Use the "screw pulling technique" if the fit is tight.
* **Action:** Place the assembled idler gear (with bearings) into its designated slot in the idler door.
* **Action:** Slide the short metal shaft through the hole in the printed part and through the bearings in the gear to lock it in place. The ends of the shaft should be flush with the surface of the plastic part.

!!! tip "Check for Free Movement"
    Place your finger on the gear and ensure it can spin freely on its shaft without any wobble or resistance.

---
### Step 20: Final Filament Path Alignment Check

This is a critical final check to ensure the two filament-driving gears are perfectly aligned with each other.

!!! warning "Perform This Check Carefully"
    Proper alignment is essential to prevent filament grinding and extrusion issues. This is your last easy chance to adjust it before closing up the extruder.

* **Action:** Temporarily hold the assembled idler door against the main extruder body, aligning the idler gear with the drive gear on the motor.
* **Action:** Take a straight piece of 1.75mm filament and push it down from the top opening of the extruder.
* **Action:** The filament should pass smoothly and straight between the grooves of both gears and down into the PTFE tube of the hotend.
* **Action:** If you feel any resistance or see misalignment, slightly loosen the grub screw on the motor's drive gear and adjust its vertical position on the shaft until the filament passes through perfectly.
* **Action:** Once you are satisfied, **firmly tighten the grub screw** on the motor's drive gear. Remember to tighten it against the flat part of the motor shaft. Finally, remove the piece of filament.

<figure markdown="1">
  ![Filament Path Alignment Check](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![Filament Path Alignment Check](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing a piece of filament passing straight between the two Bondtech gears (drive and idler) to verify alignment.</figcaption>
</figure>

---
### Step 21: Mounting the Extruder Idler Door

Now we will permanently attach the idler door to the main extruder body.

* **Action:** Place the assembled `Extruder-idler` door into its position on the `Extruder-body`.
* **Action:** Use one of the long M3x40 screws to secure it. This screw acts as the hinge pin for the door.
* **Important:** Do not overtighten this screw. The idler door must be able to pivot freely. Check its movement after tightening.

---
### Step 22: Assembling the Filament Sensor Cover

Now we will install the cover that protects the filament sensor mechanism.

* **Parts needed:**
    * `FS-cover` (1x printed part)
    * M3x10 screw (1x)
* **Action:** Place the `FS-cover` onto the extruder body, aligning it with the screw hole.
* **Action:** Insert the M3x10 screw and tighten it to secure the cover in place.
* **Pro-Tip:** If you have trouble reaching the nut inside, you can use a small Allen key to help align it with the screw.

---
### Step 23: Applying Tension to the Extruder Idler

This step is crucial for ensuring the extruder has the correct amount of grip on the filament.

* **Action:** Take the final M3x40 screw and place the idler spring over it.
* **Action:** Insert this screw-and-spring assembly into the hole on the side of the extruder that presses against the idler door you installed earlier.
* **Action:** Tighten the screw. You will feel the resistance from the spring as it compresses and applies pressure to the idler door.

!!! tip "How Much Tension is Enough?"
    A good starting point for the idler tension is to tighten the screw until the **head of the screw is approximately flush with the plastic surface** of the extruder body. This tension can be adjusted later if you experience any filament grinding (too tight) or slipping (too loose).

<figure markdown="1">
  ![Idler Tension Screw](/assets/images/image-placeholder.webp#only-light){ width="400" }
  ![Idler Tension Screw](/assets/images/image-placeholder.webp#only-dark){ width="400" }
  <figcaption>Illustration showing the head of the idler tension screw flush with the extruder body for correct starting tension.</figcaption>
</figure>

---
### Step 24: Preparing the Print Fan Support

The next steps involve installing the part cooling fan. First, let's prepare its support bracket.

* **Parts needed:**
    * `Print-fan-support` (1x printed part)
    * M3x10 screw (1x)
    * M3n nut (1x)

---
### Step 25: Assembling the Print Fan Support

First, we will assemble the bracket that will hold the main part cooling fan.

* **Action:** Take the `Print-fan-support` printed part and insert an M3n nut all the way into its hexagonal slot. Use the "screw pulling technique" if needed.
* **Action:** Place the support bracket onto the extruder body, ensuring the angled part faces downwards towards the nozzle.
* **Action:** Secure the support using an M3x10 screw.

---
### Step 26: Assembling the Fan Shroud

The fan shroud directs the airflow from the fan onto the printed part.

!!! note "Check Your Screw Length"
    The screw used in this step depends on which version of the hotend fan you installed earlier. The assembly process is the same, but you must use the correct length screw.

* **Parts needed:**
    * `Fan-shroud` (1x printed part)
    * M3nS nut (1x)
    * The correct M3 screw for your fan version (M3x20 or M3x22b)
* **Action:** Insert the M3nS square nut into the `Fan-shroud`.
* **Action:** Slide the `Fan-shroud` into place on the extruder body, making sure its protrusions fit into the corresponding grooves.
* **Action:** Secure it using the correct screw for your version. Do not overtighten.

---
### Step 27: Assembling the Part Cooling Fan

Now we'll install the main fan that cools your prints.

* **Parts needed:**
    * Print fan (1x, the larger radial fan)
    * M3x20 screw (2x)
    * M3n nut (1x)
* **Action:**
    1.  Slide the fan into the `Fan-shroud`.
    2.  Fix one side of the fan in place using one M3x20 screw.
    3.  Turn the extruder around and insert the M3n nut into the slot on the other side of the fan mount.
    4.  Secure the fan completely by inserting the second M3x20 screw from the other side. Tighten both screws carefully to avoid cracking the fan's casing.
    5.  Neatly guide the fan's cable into the designated channel on the extruder body.

---
### Step 28: Assembling the Z-Probe Sensor

This sensor is used for automatic bed leveling.

* **Parts needed:**
    * Z-Probe Sensor (e.g., SuperPINDA or similar) (1x)
* **Action:** Insert the probe into its cylindrical holder on the extruder assembly.
* **Action:** Lightly tighten the M3 screw on the holder to keep the probe from falling out.

!!! tip "Probe Height Will Be Adjusted Later"
    The final height of the probe is a critical calibration step that will be performed much later. For now, just make sure it is secure but not fully tightened.

* **Action:** Route the probe's cable into the channel alongside the other fan cable.

---
### Step 29: Mounting the Extruder to the X-Axis

This is the major step where we attach the entire completed extruder assembly to the X-axis gantry you built earlier.

* **Parts needed:**
    * Zip ties (2x)
* **Action:** Manually lower the X-axis gantry to about one-third of the way from the top.
* **Action:** Carefully align the linear bearings on the back of the extruder assembly with the smooth rods on the X-axis gantry.
* **Action:** Gently slide the extruder onto the rods. Ensure the bearings fit perfectly into the grooves on the `X-carriage` printed part.
* **Action:** Use the two zip ties to firmly secure the extruder assembly to the `X-carriage`. The zip ties pass through slots in the carriage and wrap around the bearings. Tighten them securely and trim the excess with pliers.

<figure markdown="1">
  ![Mounting Extruder to X-Axis](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Mounting Extruder to X-Axis](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Illustration showing the extruder assembly being mounted onto the X-axis rods and secured with zip ties.</figcaption>
</figure>

---
### Step 30: Final Extruder Cable Management

This is a final tidying step to ensure no wires get caught during printing.

* **Action:** Take the bundle of cables coming from the bottom of the extruder (fans and probe).
* **Action:** Neatly guide these cables over the lower smooth rod and push them back into the cable channel on the `X-carriage`. This keeps them secure and out of the way of the print area.

---
### Step 31: Installing the X-Axis Belt

Now we will install the belt that drives the X-axis.

* **Parts needed:**
    * X-axis belt (1x)
* **Action:**
    1.  Start by inserting one flat end of the belt into its slot on the `X-carriage`. Use a small screwdriver or Allen key to help push it in fully.
    2.  Route the long end of the belt through the `X-end-idler`, around the idler bearing, and back towards the extruder.
    3.  Pass the belt through the central channel in the `X-carriage`.
    4.  Continue routing the belt towards the motor and loop it around the motor's toothed pulley.
    5.  To make the next part easier, slightly loosen the screws holding the X-axis motor so you can slide it inwards to create some slack in the belt.
    6.  Insert the final flat end of the belt into the other slot on the `X-carriage`.

<figure markdown="1">
  ![X-Axis Belt Path](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![X-Axis Belt Path](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Illustration showing the complete routing path for the X-axis belt.</figcaption>
</figure>

---
### Step 32: Coarse Tensioning of the X-Axis Belt

This is the initial tensioning step. We will do fine-tuning later.

* **Action:** While holding the belt in place, pull the X-axis motor outwards (away from the idler) by hand to apply tension to the belt.
* **Action:** While maintaining this tension, tighten the screws that mount the motor to the `X-end-motor` part.
* **How it should feel:** The belt should now be straight and not sagging. You should be able to press the top and bottom parts of the belt together with your fingers with only a small amount of force.

---
### Step 33: Aligning and Testing the Belt

Before final tensioning, let's ensure the belt is aligned and the tension is reasonable.

* **Alignment:** Look at the belt from above. The top and bottom sections should be perfectly parallel to each other. If they are not, slightly loosen the grub screws on the motor pulley and adjust its position on the shaft until the belt runs straight. Then, re-tighten the grub screws.
* **Tension Test:** Hold the motor shaft firmly with a pair of pliers so it cannot turn. Now, gently try to move the extruder assembly by hand. If the tension is correct, you should feel solid resistance. If the belt is too loose, it will deform and "skip" over the teeth on the pulley. If this happens, you will need to go back to Step 31 and re-seat the belt with one less tooth to make it shorter.

---
### Step 34: Fine-Tuning the Belt Tension

This final step uses the tensioning screw we installed earlier for precise adjustments.

* **Action:** First, neatly trim any excess belt sticking out of the `X-carriage` with your pliers.
* **Action:** Locate the long tensioner screw on the back of the `X-end-motor` part.

!!! tip "Using the Tensioner Screw"
    To fine-tune the tension, you can simply turn this screw.
    * **To increase tension:** Tighten the screw (turn clockwise). This will pull the motor outwards, stretching the belt.
    * **To decrease tension:** Loosen the screw (turn counter-clockwise).
    * Make small adjustments and re-test the tension until you are satisfied.

---
### Step 35: Preparing the Cable Bundle Stiffener

The main cable bundle that goes to the extruder needs a stiffener to prevent it from sagging and getting caught on the frame during printing. We will use a piece of nylon filament for this.

* **Parts needed:**
    * Black nylon filament (1x piece)

!!! warning "Wear Safety Glasses"
    The nylon filament can be stiff and sharp when cut. It is recommended to wear safety glasses for this step.

* **Action:** Take the piece of thick, black nylon filament.
* **Action:** Using your pliers, cut one end of the filament at a sharp angle to create a point. This will make it much easier to insert into the cable sleeve in a later chapter.

---
### Step 36: Installing the Cable Stiffener

Now we will insert the nylon filament guide that you prepared earlier. This acts as a stiff backbone for the main cable bundle.

!!! danger "Be Extremely Careful"
    This step requires you to push a stiff object with pliers in a tight space with many delicate wires. The pliers can easily slip and damage a cable. Proceed slowly and with great care.

* **Action:** Locate the small hole for the nylon filament on the `X-carriage`, just above the bottom linear bearing.
* **Action:** Using your pliers to grip the pointed end of the nylon filament, carefully insert it into the hole. You may need to twist the filament as you push it in to help it find its path.
* **Action:** Push it in until it is securely seated. A gentle pull should be met with strong resistance.

---
### Step 37: Assembling the Back Cover and Cable Holder

Let's assemble the back cover which will enclose the extruder assembly and manage the main cable bundle.

* **Parts needed:**
    * `X-carriage-back` (1x printed part)
    * `Cable-holder` (1x printed part)
    * M3x40 screw (1x)
    * M3n nut (1x)
* **Action:** Take the `X-carriage-back` part and insert the M3n nut into its hexagonal slot.
* **Action:** Attach the `Cable-holder` part to the `X-carriage-back` using the long M3x40 screw. Ensure the U-shaped slots on both parts are aligned.

---
### Step 38: Mounting the Back Cover

This step involves routing all the extruder cables through the back cover.

* **Action:** Carefully push the main bundle of cables from the extruder (IR-sensor, extruder motor, hotend fan, print fan, and Z-probe) THROUGH the large opening in the `X-carriage-back` assembly.
* **Important:** The two cables from the hotend (the thick heater wires and the thin thermistor wires) do **not** go through this opening. They will be secured separately.
* **Action:** Also guide the nylon stiffener through its dedicated hole in the back cover.
* **Action:** Slide the `X-carriage-back` into place against the rear of the extruder assembly.
* **Action:** Secure the back cover with four M3x10 screws. As you tighten, double-check that no wires are being pinched between the parts.

<figure markdown="1">
  ![Back Cover Cable Routing](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Back Cover Cable Routing](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Illustration showing the correct path for the cables through the back cover.</figcaption>
</figure>

---
### Step 39: Wrapping the Main Cable Bundle

This is the final and most important cable management step. A neat and secure cable bundle is essential for reliable operation.

* **Parts needed:**
    * Textile sleeve (the largest one from your kit)
    * Zip ties (5x)
* **Action:**
    1.  Take the textile sleeve and wrap it around the main cable bundle coming from the extruder. Make sure to include the black nylon stiffener inside the sleeve. Leave the hotend cables out for now.
    2.  Slide the end of the sleeve into the `Cable-holder` part. Gently twist the sleeve to tighten it around the cables.
    3.  Use three zip ties to firmly secure the sleeve to the **lower row** of slots on the `Cable-holder`. Trim the excess from the zip ties as flush as possible.
    4.  Now, take the two hotend cables. **It is important that the thin thermistor wire is routed *above* the thicker heater wire.**
    5.  Place these two hotend cables into the upper channel of the `Cable-holder`.
    6.  Use the remaining two zip ties to secure the hotend cables to the **upper row** of slots on the `Cable-holder`.
    7.  Finally, continue wrapping the textile sleeve around the entire bundle of cables, including the newly added hotend wires.

---
### Step 40: E-Axis is Finished!

!!! success "Congratulations! The Hardest Part is Over!"
    You have just completed the most complex chapter of the entire build. The E-axis assembly is finished! Take a moment to admire your work. Check that all cables are secure and that nothing is pinched. You're getting very close to the finish line now.