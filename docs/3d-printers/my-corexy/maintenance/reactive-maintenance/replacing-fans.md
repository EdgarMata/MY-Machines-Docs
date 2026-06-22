# Replacing Fans

Fans are mechanical components with a limited lifespan. When a fan fails, it must be replaced immediately to prevent other components from overheating. This guide covers replacing the hotend cooling fan and the part cooling fan.

!!! danger "Safety First: Cool Down and Unplug"
    Ensure the printer is off and completely cool before starting work.

### Replacing the Hotend Cooling Fan (Heatsink Fan)

This fan is critical. Its job is to cool the heatsink to prevent "heat creep" and clogs. If this fan fails, your hotend will jam quickly.

1.  **Access the Fan**: Remove the front toolhead shroud to access the fan.
2.  **Unmount Fan**: Unscrew the four bolts that hold the fan to the hotend's heatsink.
3.  **Disconnect and Install New Fan**: Disconnect the old fan's plug. Install the new fan in its place.
4.  **Check Airflow Direction**:
    !!! warning "Airflow Direction is Critical"
        The hotend fan **MUST** blow air **INTO** the heatsink. Most fans have small arrows on the plastic casing indicating the direction of rotation and the direction of airflow. Confirm this before tightening the screws.

<figure markdown="1">
  ![Checking airflow direction on a new fan](/images/image-placeholder.png#only-light){ width="500" }
  ![Checking airflow direction on a new fan](/images/image-placeholder.png#only-dark){ width="500" }
  <figcaption>A cooling fan with small arrows embossed on its side, indicating the direction of blade rotation and the direction of airflow.</figcaption>
</figure>

### Replacing the Part Cooling Fan

This fan cools the plastic as it is being extruded, which is essential for overhangs and print quality.

1.  **Access the Fan**: The part cooling fan is typically a "blower" style fan mounted to the toolhead shroud or ducting. Unscrew it from its mount.
2.  **Disconnect and Install New Fan**: Disconnect the old fan and install the new one.
3.  **Check Orientation**: Ensure the new fan is oriented correctly so that its output is aimed at the printed part, just below the nozzle.

<figure markdown="1">
  ![Mounting a part cooling fan](/images/image-placeholder.png#only-light){ width="600" }
  ![Mounting a part cooling fan](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A blower-style part cooling fan being mounted onto the side of a toolhead shroud.</figcaption>
</figure>