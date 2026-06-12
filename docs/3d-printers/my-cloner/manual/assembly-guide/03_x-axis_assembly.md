# Chapter 3: X-Axis Assembly

In this chapter, we will build the X-axis. This is the gantry that moves from left to right across the printer, and it will eventually carry the extruder and hotend assembly. A precise and rigid X-axis is key for accurate prints.

---
### Step 1: Tools Necessary for This Chapter

Before you begin, gather the tools you will need for this section of the build.

* **Tools needed:**
    * 2.5mm Allen key
    * 2mm Allen key

---
### Step 2: X-Axis - Preparing X-End Parts (Part 1)

Let's start by gathering the main printed parts and the bearings for the X-axis assembly.

* **Parts needed:**
    * `X-end-motor` (1x printed part)
    * `X-end-idler` (1x printed part)
    * Linear bearings (4x)

---
### Step 3: X-Axis - Preparing X-End Parts (Part 2)

Now gather the hardware that will be installed into the X-End parts.

* **Parts needed:**
    * M3x30 screw (1x)
    * M3x18 screw (1x)
    * M3nN nyloc nut (1x)
    * M3nS square nut (1x)
    * `623h` bearing with housing (1x)

---
### Step 4: X-Axis - Inserting Linear Bearings

The first assembly action is to press the linear bearings into the two main plastic parts.

* **Action:** Gently press two linear bearings into each of the two X-End printed parts (`X-end-motor` and `X-end-idler`).
* **Important:** The bearings should be pushed in until they are flush with the top surface or until they hit the internal stop inside the printed part. Do not try to force them past this point.

!!! tip "Optimize Bearing Alignment for Longevity"
    For smoother movement and less wear on the rods, try to orient the two bearings in each part so their internal ball tracks are offset by 45 degrees from each other. This distributes the load more evenly across the smooth rods.

<figure markdown="1">
  ![Bearing 45-degree offset](../../images/image-placeholder.png#only-light){ width="400" }
  ![Bearing 45-degree offset](../../images/image-placeholder.png#only-dark){ width="400" }
  <figcaption>Illustration showing two bearings with their internal ball tracks rotated 45 degrees relative to each other.</figcaption>
</figure>

---
### Step 5: X-End-Motor - Tensioner Assembly

Now, let's prepare the belt tensioning mechanism on the motor-side part.

* **Action:** Take the `X-end-motor` part. Insert the M3nS square nut all the way into its slot.
* **Action:** Insert the long M3x30 screw through the hole. For now, just screw it in a few turns to hold it in place. Leave a gap of about 2mm between the screw head and the plastic part. We will adjust this later to tension the belt.

---
### Step 6: X-End-Idler - Bearing Assembly

Next, we will install the idler bearing on the opposite side.

* **Action:** Take the `X-end-idler` part and insert the M3nN nyloc nut into its hexagonal slot.
* **Action:** Insert the `623h` idler bearing into its designated space.
* **Action:** Secure the bearing in place using the M3x18 screw. Tighten it, but then check that the bearing can still spin freely. If not, loosen the screw slightly.

---
### Step 7: X-Axis - Preparing the Smooth Rods

* **Action:** Identify the **longest** pair of smooth rods in your kit. These are for the X-axis.
* **Action:** It's a good idea to have some paper towels ready to wipe any excess oil from the rods.

---
### Step 8: Marking the Bearings (Optional Pro-Tip)

This optional step makes the alignment from Step 4 much easier to verify.

!!! tip "Mark Your Bearings"
    * **Action:** Before assembling the gantry, you can use a permanent marker to draw a small line on the outer casing of each linear bearing, directly above one of the internal rows of balls.
    * **Benefit:** When you later insert the rods, you can use these marks to visually confirm that the bearings are oriented correctly and offset by 45 degrees.

---
### Step 9: X-Axis Assembly

Now we will connect the two prepared X-End parts to form the complete gantry.

!!! warning "Handle with Care"
    Be very gentle when inserting the rods into the bearings. Do not tilt them, and do not use excessive force. Forcing a rod can dislodge the small ball bearings inside the linear bearing, ruining it. The fit should be snug but smooth.

* **Action:** Take one smooth rod and carefully slide it through the two bearings in the `X-end-motor` part.
* **Action:** Take the `X-end-idler` part and slide it onto the other end of the same rod.
* **Action:** Repeat the process with the second smooth rod, inserting it through the remaining set of bearings on both X-end parts. Push both ends together to form the complete gantry.

---
### Step 10: Assembling the X-Axis Motor Pulley (Part 1)

The final step in this section is to prepare the motor.

* **Parts needed:**
    * X-axis motor (1x)
    * GT2-16 pulley (1x)
* **Action:** Ensure you are using the motor specifically labeled for the **X-axis**, as cable lengths may differ.

---
### Step 11: Assembling the X-Axis Motor Pulley (Part 2)

This step is critical for ensuring the motor can reliably drive the belt without slipping.

* **Action:** Take the GT2-16 pulley and slide it onto the X-axis motor shaft.

!!! danger "Critical Step: Pulley Alignment"
    The motor shaft has a flat side (a "D" shape). You **must** align one of the small grub screws on the pulley so that it tightens directly against this flat part. This provides a secure lock and prevents the pulley from slipping under load. Slightly tighten both grub screws for now.

* **Action:** Do not press the pulley all the way against the motor's body. Leave a small gap (about 1mm) to ensure it can rotate freely without rubbing.

<figure markdown="1">
  ![Motor Pulley Alignment](../../images/image-placeholder.png#only-light){ width="400" }
  ![Motor Pulley Alignment](../../images/image-placeholder.png#only-dark){ width="400" }
  <figcaption>A close-up showing the flat part of the motor shaft and a grub screw being tightened against it.</figcaption>
</figure>

---
### Step 12: X-Axis - Assembling the Motor

Now, let's mount the prepared motor onto the X-axis gantry.

* **Parts needed:**
    * M3x18 screw (3x)
* **Action:** Take the motor with the pulley attached and place it onto the `X-end-motor` printed part.
* **Action:** Secure the motor using the three M3x18 screws. Make sure the motor is oriented correctly so its cable connector points in the intended direction for cable management.

---
### Step 13: X-Axis is Finished!

The X-axis gantry is now fully assembled!

* **Action:** Give your assembly a final look-over. Compare it to the reference picture to ensure everything looks correct and is securely fastened.

!!! success "Ready for the Next Stage"
    With the X-axis done, it's time to build the Z-axis, which will lift this entire assembly up and down.

<figure markdown="1">
  ![Completed X-Axis](../../images/image-placeholder.png#only-light){ width="610" }
  ![Completed X-Axis](../../images/image-placeholder.png#only-dark){ width="610" }
  <figcaption>The fully assembled X-axis, ready for the next chapter.</figcaption>
</figure>
