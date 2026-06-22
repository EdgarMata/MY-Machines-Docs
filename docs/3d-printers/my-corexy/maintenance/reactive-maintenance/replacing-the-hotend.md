# Replacing the Full Hotend Assembly

Sometimes, a simple cleaning or part replacement isn't enough. A catastrophic leak that encases the heater block in plastic, a broken heatbreak, or simply upgrading to a new model may require replacing the entire hotend assembly.

!!! danger "Safety First: Hot Components & Electricity"
    Before you begin, ensure the printer is completely cool and **unplugged from the wall outlet.**

### Procedure

1.  **Access the Hotend**: First, you need to get clear access to the hotend. On the Stealthburner toolhead, this typically involves removing the front fan shroud and possibly the part cooling fan duct.

2.  **Disconnect Wiring**: Carefully disconnect the wires for the heater cartridge, thermistor, and the hotend cooling fan. If you have a toolhead PCB, unplug them from the board. Otherwise, disconnect them from their respective connectors in the wiring harness.

<figure markdown="1">
  ![Accessing the hotend assembly](/images/image-placeholder.png#only-light){ width="700" }
  ![Accessing the hotend assembly](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>The toolhead with its front cover removed, showing the hotend assembly, its mounting screws, and wiring connections.</figcaption>
</figure>

3.  **Unmount the Old Hotend**: Locate the main mounting screws that hold the hotend to the extruder body (e.g., the "groove mount"). Unscrew these and carefully remove the entire hotend assembly from the toolhead.

4.  **Install the New Hotend**: Mount the new hotend assembly, making sure it is fully seated and aligned correctly. Fasten the mounting screws securely.

5.  **Reconnect Wiring**: Neatly connect the wires for the new heater, thermistor, and fan. Ensure the connections are secure and there are no exposed wires that could short.

6.  **Reassemble Toolhead**: Re-attach the toolhead shroud and any other parts you removed.

!!! warning "Calibration is Mandatory After Replacement"
    After replacing the entire hotend, you **must** perform the following calibrations before printing:
    * **PID Tune**: The new heater will have different properties. A PID tune is essential for stable temperatures.
    * **Z-Offset Calibration**: The new hotend's length may be slightly different. You must re-calibrate your Z-offset to get a correct first layer.