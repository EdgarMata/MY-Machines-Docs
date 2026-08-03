# Chapter 07: A/B Belts

This chapter focuses on installing the two belts that drive the CoreXY motion system. Correct belt routing and tension are absolutely essential for print quality, preventing issues like ringing and dimensional inaccuracies.

!!! info "The CoreXY Principle"
    CoreXY systems use two long belts, typically named A and B. The combined movement of these two belts is what allows the toolhead to move to any XY coordinate. For this to work correctly, both belts must have equal tension. A good trick is to run the first belt, cut it to the perfect length, and then cut the second belt to the exact same length before installing it.

<figure markdown="1">
  ![Overview of the A and B belt paths](/assets/images/image-placeholder.webp#only-light){ width="800" }
  ![Overview of the A and B belt paths](/assets/images/image-placeholder.webp#only-dark){ width="800" }
  <figcaption>Two separate diagrams, one showing the complete path of the 'A' belt and another showing the path of the 'B' belt.</figcaption>
</figure>

### Step 1: Prepare the X-Carriage

The X-carriage not only holds the toolhead but also serves as the anchor point for the A and B belts.

1.  Install the required M3 heat-set inserts into the printed carriage parts.
2.  Loosely assemble the two main pieces of the X-carriage onto the MGN12 linear rail. This will clamp the belts in later steps.

<figure markdown="1">
  ![Assembling the X-carriage parts](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Assembling the X-carriage parts](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>The printed parts of the X-carriage being assembled onto the MGN12 linear rail on the X-axis.</figcaption>
</figure>

### Step 2: Route the Belts

Routing the belts can be tricky. Use tweezers to help guide the belt around the pulleys and bearings.

1.  **Anchor the Belts**: Start by clamping one end of both the A and B belts into one side of the X-carriage. The belt teeth should face outwards, away from the extrusion.
2.  **Route the A-Belt**: Carefully follow the diagram, routing the A-belt from the X-carriage, around the A-drive pulley, across the back to the B-idler, and back to the X-carriage.
3.  **Route the B-Belt**: In the same manner, route the B-belt from the X-carriage, around the B-drive pulley, across the back to the A-idler, and back to the X-carriage.

<figure markdown="1">
  ![Routing a belt around a drive pulley and idler](/assets/images/image-placeholder.webp#only-light){ width="700" }
  ![Routing a belt around a drive pulley and idler](/assets/images/image-placeholder.webp#only-dark){ width="700" }
  <figcaption>A close-up diagram showing the path of a belt as it makes its way around the bearings of a drive or idler assembly.</figcaption>
</figure>

### Step 3: Tension and Secure the Belts

1.  Feed the loose ends of both belts back into the open side of the X-carriage.
2.  Lightly tighten the screws so the belts are held but can still be pulled through.
3.  Using a pair of pliers, pull the end of one belt until it is taut.
4.  While maintaining tension, fully tighten the screws on the X-carriage to lock the belt in place.
5.  Repeat for the second belt, trying to match the tension of the first one as closely as possible. You can pluck the belts like a guitar string to compare their frequency.

<figure markdown="1">
  ![Tensioning and securing the belts at the X-carriage](/assets/images/image-placeholder.webp#only-light){ width="700" }
  ![Tensioning and securing the belts at the X-carriage](/assets/images/image-placeholder.webp#only-dark){ width="700" }
  <figcaption>Illustration showing pliers pulling a belt tight at the X-carriage before the final screws are tightened to clamp it down.</figcaption>
</figure>

### Step 4: Install the Inductive Probe

With the belts installed, you can now mount the inductive probe to the X-carriage. Set its initial position so the tip is about 6mm below the bottom of the plastic part. This can be fine-tuned later.
