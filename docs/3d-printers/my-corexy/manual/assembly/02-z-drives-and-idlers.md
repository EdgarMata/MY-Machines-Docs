# Chapter 02: Z-Drives and Idlers

In this chapter, we will build and install the entire Z-axis motion system. This includes the four Z-drives which house the motors, the four Z-idlers, the linear rails for the gantry to move on, and the electronics deck panel.

<figure markdown="1">
  ![Overview of Z-axis components](/images/image-placeholder.png#only-light){ width="700" }
  ![Overview of Z-axis components](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>An overview graphic showing the fully assembled frame with the key components of this chapter highlighted: Z-drives, Z-idlers, Z-linear rails, and the deck panel.</figcaption>
</figure>

### Section 1: Z-Axis Linear Rails

The linear rails guide the Z-axis movement and must be prepared and installed correctly for smooth operation.

!!! warning "Handle Rails With Care"
    The carriage can easily slide off the rail. Dropping the carriage will likely damage the internal ball bearings. Any nicks or dents on the rail can cause binding or rough motion.

1.  **Preparation**: Most rails ship with a protective oil. Clean this off thoroughly with isopropyl alcohol, then apply a proper lubricant (like Mobilux EP2 grease) to the carriage bearings.
2.  **Installation**: Install the four MGN9 linear rails onto the four vertical extrusions of the frame.
    * Use a printed alignment tool to ensure the rail is perfectly centered on the extrusion.
    * Leave a small gap of about 3mm between the bottom of the rail and the bottom frame extrusion.
    * When tightening the M3x8 SHCS screws, start from the center and work your way outwards.
    * Once installed, use a piece of tape to secure the carriage so it does not fall off in later steps.

<figure markdown="1">
  ![Installing a Z-axis linear rail with an alignment tool](/images/image-placeholder.png#only-light){ width="600" }
  ![Installing a Z-axis linear rail with an alignment tool](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A close-up showing a printed MGN9 alignment guide being used to position the linear rail in the center of the vertical extrusion before tightening the screws.</figcaption>
</figure>

### Section 2: Deck Panel

The deck panel serves as the mounting surface for your electronics.

1.  **Flip Printer**: Carefully turn the entire frame upside down. This makes installation much easier. Ensure your linear rail carriages are secured first!
2.  **Install Panel**: Place the deck panel onto the bottom extrusions. The side with the large cutout notch should face the back of the printer.
3.  **Install DIN Rails**: Mount the two metal DIN rails onto the deck panel. These will hold your power supplies and other electronics.

<figure markdown="1">
  ![Installing the deck panel and DIN rails](/images/image-placeholder.png#only-light){ width="700" }
  ![Installing the deck panel and DIN rails](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>The printer frame shown upside down, with the deck panel and the two DIN rails being mounted.</figcaption>
</figure>

### Section 3: Z-Drive Assembly

This is a detailed sub-assembly. We will build four of these units.

1.  **Preparation**: Begin by installing the M3 heat-set inserts into all the printed parts for the Z-drives.
2.  **Belt Drive Sub-Assembly**: Assemble the GT2 80T pulley, three 625 bearings, shims, and the 5x60mm shaft.
3.  **Use Thread Locker**: Apply thread locker to the set screws on the GT2 20T pulley before inserting it onto the shaft. This is critical for preventing future issues.
4.  **Combine**: Insert the closed-loop GT2 188mm belt and place the belt drive sub-assembly into the main printed housing, securing it with M3x40 SHCS.
5.  **Motor Assembly**: Attach the GT2 16T pulley to the NEMA17 motor shaft. Note the specific 10.7mm distance shown in the diagram. Mount the motor to its printed bracket.

<figure markdown="1">
  ![Exploded view of the Z-drive assembly](/images/image-placeholder.png#only-light){ width="800" }
  ![Exploded view of the Z-drive assembly](/images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>An exploded diagram showing all the individual components of the Z-drive: motor, pulleys, bearings, shaft, and printed parts.</figcaption>
</figure>

### Section 4: Z-Drive Installation

With the printer still upside down, install the four Z-drive assemblies onto the four corners of the frame.

1.  Use M5 T-Nuts and M5x40 SHCS screws to loosely attach the assembly to the frame.
2.  Slide the motor assembly into place at an angle.
3.  Secure the motor with an M5x10 BHCS, but do not tighten it yet.
4.  Flip the belt tensioner latch closed. This will apply tension to the belt.
5.  Now, fully tighten all the mounting bolts.
6.  Attach a rubber foot to the top of the drive assembly.
7.  Repeat this process for the other three corners, noting that some printed parts are mirrored.

<figure markdown="1">
  ![Installing a Z-drive assembly onto the frame](/images/image-placeholder.png#only-light){ width="700" }
  ![Installing a Z-drive assembly onto the frame](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>Illustration of a completed Z-drive unit being slid into place on a corner of the upside-down frame.</figcaption>
</figure>

### Section 5: Z-Idler Installation

The Z-idlers guide the belts at the top of the printer.

1.  **Assembly**: Build the four Z-idler assemblies. This involves inserting an M3 nut and attaching the GT2 20T idler with an M5x30 BHCS.
2.  **Installation**: Flip the printer right-side up. Install one Z-idler assembly in each of the four top corners of the frame.
3.  **Orientation**: Ensure the idler is oriented to align with the pulley in the Z-drive directly below it. Press the idler firmly into the corner before tightening.

<figure markdown="1">
  ![Installing a Z-idler assembly](/images/image-placeholder.png#only-light){ width="600" }
  ![Installing a Z-idler assembly](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A Z-idler assembly being mounted in a top corner of the frame with M5 T-nuts and screws.</figcaption>
</figure>