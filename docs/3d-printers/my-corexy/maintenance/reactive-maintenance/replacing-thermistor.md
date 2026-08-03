# Replacing the Thermistor

The thermistor is the small sensor that reports the hotend's temperature to the controller board. Its wires are very delicate and can break over time. If you get a "Heater not heating at expected rate" or a similar thermal error, a faulty thermistor is a likely culprit.

!!! danger "Safety First: Cool Down and Unplug"
    Ensure the printer is off and completely cool before beginning.

### Procedure

1.  **Access the Heater Block**: Remove the toolhead shroud and silicone sock.

2.  **Disconnect Old Thermistor**: Unplug the old thermistor's connector.

3.  **Remove Old Thermistor**: The thermistor is held in place by a very small screw and washer. Carefully loosen and remove this screw, then gently pull the old thermistor's glass bead and wires out of the block.

<figure markdown="1">
  ![Removing the thermistor from the heater block](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Removing the thermistor from the heater block](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>A close-up of the heater block showing the small screw and delicate wires of the thermistor being gently removed.</figcaption>
</figure>

4.  **Insert New Thermistor**: Carefully slide the glass bead of the new thermistor into its designated hole in the heater block.

5.  **Secure New Thermistor**: This is a critical step.
    !!! warning "Do Not Crush the Wires"
        Gently tighten the retaining screw. The screw and washer should press on the wire's insulation to hold it in place, not on the bare wire itself. **Overtightening will crush the delicate wires, causing a short and ruining the new thermistor.** It only needs to be snug enough to prevent the thermistor from falling out.

6.  **Reconnect and Reassemble**: Plug in the new thermistor and reassemble the toolhead.

7.  **Test**: Power on the printer and check your web interface. Verify that the hotend is reporting a normal room temperature before attempting to heat it.
