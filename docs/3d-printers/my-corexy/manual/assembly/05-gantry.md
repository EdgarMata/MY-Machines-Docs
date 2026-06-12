# Chapter 05: The Gantry

The gantry is the heart of the CoreXY motion system. It's the assembly that moves in the X and Y directions, carrying the toolhead. This chapter covers the construction of the Y-axis arms, the X-axis rail, and how to combine them with the A/B drives and idlers from the previous chapter to form the complete gantry.

<figure markdown="1">
  ![Overview of the gantry components](../../images/image-placeholder.png#only-light){ width="800" }
  ![Overview of the gantry components](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>An overview graphic showing all the components that form the gantry: the A/B drives and idlers, the X and Y extrusions, linear rails, and the XY joints.</figcaption>
</figure>

### Section 1: Y-Axis Arms

You will build two Y-axis arms, which are mirror images of each other.

1.  **Prepare Extrusions**: Take your Y-axis aluminum extrusions and insert the required M3 and M5 T-Nuts into the channels as shown in the diagrams.
2.  **Mount Linear Rails**: Attach an MGN9 linear rail to each Y-axis extrusion. Use a printed alignment tool to keep it centered. Remember to secure the carriage with tape to prevent it from falling off.
3.  **Attach End Pieces**: Fasten the printed idler-end pieces (which hold the Y-axis belt idlers) to the front of each Y-axis arm. Ensure they sit perfectly flush with the end of the extrusion.

<figure markdown="1">
  ![Assembling a Y-axis arm](../../images/image-placeholder.png#only-light){ width="700" }
  ![Assembling a Y-axis arm](../../images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>Illustration of a Y-axis extrusion with the linear rail mounted and the printed idler-end piece being attached.</figcaption>
</figure>

### Section 2: XY Joints

The XY Joints connect the X-axis rail to the Y-axis arms. You will build one left and one right mirrored joint.

1.  **Preparation**: Install the M5 nuts into the printed joint housings.
2.  **Bearing Stacks**: For each joint, create the bearing stacks on the integrated posts using F695 bearings and M5 shims. An M5 bolt can be used as a temporary alignment aid.
3.  **Install Idler**: Screw the GT2 20T idler into place. Do not overtighten this bolt; the idler must spin freely.

<figure markdown="1">
  ![Exploded view of an XY Joint assembly](../../images/image-placeholder.png#only-light){ width="600" }
  ![Exploded view of an XY Joint assembly](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>An exploded diagram showing the components of a single XY joint: printed parts, bearings, shims, idler, and screws.</figcaption>
</figure>

### Section 3: X-Axis Rail

Prepare the X-axis rail by mounting the MGN12 linear rail onto the X-axis extrusion. As before, use an alignment tool and secure the carriage with tape. Prepare the rail by inserting the necessary T-Nuts for the X-carriage and belt clamps.

<figure markdown="1">
  ![Preparing the X-axis rail](../../images/image-placeholder.png#only-light){ width="700" }
  ![Preparing the X-axis rail](../../images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>The X-axis extrusion with the MGN12 linear rail being mounted and T-nuts inserted into the channel.</figcaption>
</figure>

### Section 4: Final Gantry Assembly

Now it's time to connect everything together.

1.  **Attach Y-Arms to Drives**: Connect the two Y-axis arms you built in Section 1 to the A-Drive and B-Drive assemblies from the previous chapter. This will form the back and sides of the gantry.
2.  **Attach XY Joints to Y-Arms**: Slide the left and right XY Joints onto the carriages of the Y-axis linear rails and secure them.
3.  **Install X-Axis**: Fit the X-axis rail between the two XY Joints and fasten it securely. Your gantry should now be a single, rigid assembly.

<figure markdown="1">
  ![The fully assembled gantry](../../images/image-placeholder.png#only-light){ width="800" }
  ![The fully assembled gantry](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>Illustration of the final, fully assembled gantry, showing all components connected together.</figcaption>
</figure>