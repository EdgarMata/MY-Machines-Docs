# Step 09: Component Mounting

This chapter guides you through the physical installation of each electronic component onto the deck panel and DIN rails.

### Step 1: Raspberry Pi

Mount the Raspberry Pi to the deck panel using four M2x10 self-tapping screws. The ports should face outwards for easy access.

<figure markdown="1">
  ![Mounting the Raspberry Pi](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![Mounting the Raspberry Pi](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>The Raspberry Pi being secured to the deck panel with self-tapping screws.</figcaption>
</figure>

### Step 2: Power Supplies (PSUs)

You will mount two power supplies: a small 5V PSU for the Raspberry Pi and a large 24V PSU for the rest of the printer's components.

* **5V PSU**: Mount the RS-25-5 (or similar) PSU using M3x6 BHCS.
* **24V PSU**: Mount the LRS-200-24 (or similar) PSU to its DIN rail bracket using M4x6 BHCS, then clip the entire assembly onto one of the DIN rails.

<figure markdown="1">
  ![Mounting the 24V and 5V Power Supplies](/assets/images/image-placeholder.webp#only-light){ width="700" }
  ![Mounting the 24V and 5V Power Supplies](/assets/images/image-placeholder.webp#only-dark){ width="700" }
  <figcaption>The 24V PSU mounted on its DIN rail bracket, and the smaller 5V PSU mounted directly to the deck panel.</figcaption>
</figure>

### Step 3: Controller Board

Mount your main controller board (e.g., Bigtreetech Octopus) using its printed mounting brackets. These are typically secured with M2x10 self-tapping screws.

<figure markdown="1">
  ![Mounting the Controller Board](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Mounting the Controller Board](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>The main controller board being attached to the deck panel using its printed mounting feet.</figcaption>
</figure>

### Step 4: Mains Power Inlet and SSR

* **Power Inlet**: Assemble the filtered mains power inlet, which includes the switch and fuse holder. This assembly mounts on the back of the printer.
* **Solid State Relay (SSR)**: Attach the SSR to its metal DIN rail clip using M4x6 BHCS, then snap it onto the second DIN rail. The SSR is used to safely switch the AC power for the heated bed.

<figure markdown="1">
  ![Mounting the Power Inlet and SSR](/assets/images/image-placeholder.webp#only-light){ width="700" }
  ![Mounting the Power Inlet and SSR](/assets/images/image-placeholder.webp#only-dark){ width="700" }
  <figcaption>The assembled power inlet ready for installation, and the Solid State Relay (SSR) clipped onto a DIN rail.</figcaption>
</figure>

### Step 5: Endstops

Prepare and mount the endstop switches.

* **Z-Endstop**: Assemble the Z-endstop microswitch into its printed housing. The pulley must be press-fit securely. Mount this assembly to the rear extrusion of the frame.
* **X/Y Endstops**: Solder short lengths of wire to the C (Common) and NC (Normally Closed) terminals of two microswitches. These will be installed on the gantry later.

<figure markdown="1">
  ![Assembling the Z-Endstop](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Assembling the Z-Endstop](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>The Z-endstop microswitch being installed into its printed housing and mounted on the frame.</figcaption>
</figure>
