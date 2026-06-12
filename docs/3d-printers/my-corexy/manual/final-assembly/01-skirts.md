# Chapter 14: Skirts

The skirts enclose the electronics bay at the bottom of the printer. They serve to protect the electronic components from dust and debris, aid in cooling by directing airflow, and give the printer a clean, finished appearance.

### Step 1: Preparation

Before installation, a few of the printed skirt parts require some preparation.

1.  **Heat-Set Inserts**: Install all the required M3 heat-set inserts into the various skirt pieces. The front skirt in particular requires inserts on its inner face for the LCD mount.
2.  **Remove Built-in Support**: The main front skirt piece is printed with a thin, built-in support for better printability. Carefully remove this highlighted section with flush cutters or a hobby knife.

<figure markdown="1">
  ![Preparing the front skirt piece](../../images/image-placeholder.png#only-light){ width="700" }
  ![Preparing the front skirt piece](../../images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>The front skirt piece, showing the location of the built-in support to be removed and the heat-set inserts to be installed.</figcaption>
</figure>

### Step 2: LCD Screen Assembly

The front skirt houses the Mini 12864 display.

1.  Mount the LCD screen to its printed bracket using M3x12 SHCS.
2.  Attach the entire screen assembly to the inside of the front skirt.
3.  Connect the two flat ribbon cables (EXP1 and EXP2) to the back of the screen. These will be routed to the controller board later.

<figure markdown="1">
  ![Assembling the LCD screen into the front skirt](../../images/image-placeholder.png#only-light){ width="600" }
  ![Assembling the LCD screen into the front skirt](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>An exploded view showing the Mini 12864 screen, its printed bracket, and the front skirt piece.</figcaption>
</figure>

### Step 3: Skirt Installation

Attach the skirt sections around the bottom perimeter of the printer frame using M3x8 SHCS and M3 T-Nuts that you slide into the frame's channels.

!!! tip "Keystone Inserts"
    The rear skirt piece has cutouts for keystone jacks. You can install blanks or add modules for USB or Ethernet ports, connecting them to your Raspberry Pi for easy access.

<figure markdown="1">
  ![Installing the side and rear skirts](../../images/image-placeholder.png#only-light){ width="800" }
  ![Installing the side and rear skirts](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>The printer frame with several skirt sections being attached to the bottom extrusions with T-Nuts and screws.</figcaption>
</figure>

### Step 4: Electronics Cooling Fan

One of the side skirts houses a 60mm fan to cool the electronics bay. Mount the fan so that it blows air *into* the electronics compartment. Route the wires and connect them to an available fan port on your controller board.

### Step 5: Bottom Panel and Z-Belt Covers

1.  **Bottom Panel**: Attach the bottom electronics panel using strips of VHB double-sided tape. This seals the electronics bay.
2.  **Z-Belt Covers**: To prevent the Z-belts from rubbing against the bottom panel, install the four small, printed Z-belt covers. These attach to the frame with M3 screws and hammerhead nuts.

<figure markdown="1">
  ![Installing the Z-belt covers](../../images/image-placeholder.png#only-light){ width="600" }
  ![Installing the Z-belt covers](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A close-up view showing a Z-belt cover being slid into place over a Z-belt and secured with a hammerhead nut.</figcaption>
</figure>