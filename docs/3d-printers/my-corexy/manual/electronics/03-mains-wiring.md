# Step 11: Mains and PSU Wiring

!!! danger "Lethal Voltage - Proceed with Extreme Caution"
    This chapter deals with 110V/230V mains electricity. A mistake here can lead to electric shock, fire, or death. **If you are not experienced and confident, STOP and consult a qualified electrician.**
    * Always work with the printer unplugged.
    * Use appropriately gauged wire (1mm² / AWG18 or thicker).
    * Ensure all connections are secure and fully insulated.
    * Protective Earth (Ground) is not optional. It is a critical safety feature.

### Step 1: Set PSU Input Voltage

Check the side of your main 24V PSU for a small, recessed switch. Make sure it is set to the correct voltage for your region (e.g., 115V or 230V).

<figure markdown="1">
  ![PSU input voltage switch](../../images/image-placeholder.png#only-light){ width="400" }
  ![PSU input voltage switch](../../images/image-placeholder.png#only-dark){ width="400" }
  <figcaption>A close-up of the input voltage selection switch on the 24V power supply.</figcaption>
</figure>

### Step 2: AC Mains Wiring

1.  **Inlet to Switch**: Wire Live and Neutral from your filtered mains inlet to the main power switch.
2.  **Switch to Components**: From the switch, distribute Live (L) and Neutral (N) to the AC inputs of your 24V PSU, your 5V PSU, and the AC input side of the Solid State Relay (SSR).
3.  **Heater Bed**: Connect the two AC power wires from your heated bed to the AC load side of the SSR.
4.  **Grounding**: Run a Protective Earth (PE) wire from the mains inlet to the earth connection on the 24V PSU, the 5V PSU, the metal frame of the printer, and the ground screw on your heated bed.

<figure markdown="1">
  ![AC mains wiring diagram](../../images/image-placeholder.png#only-light){ width="800" }
  ![AC mains wiring diagram](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>A clear wiring diagram showing connections from the inlet to the switch, PSUs, and SSR. Protective Earth connections are highlighted and shown connecting to all major components.</figcaption>
</figure>

### Step 3: DC Power Wiring

1.  **24V Power**: Run wires from the 24V DC output (+V and -V) of the main PSU to the main power inputs on your controller board. You will likely need to power both the `PWR IN` and `MOT PWR IN` terminals.
2.  **5V Power**: Run wires from the 5V DC output of the smaller PSU to the Raspberry Pi's GPIO pins to provide it with power.
3.  **SSR Control**: Run a pair of wires from a heater output on your controller board (e.g., `BED_OUT`) to the DC control terminals (+ and -) on the SSR.

<figure markdown="1">
  ![DC power distribution diagram](../../images/image-placeholder.png#only-light){ width="800" }
  ![DC power distribution diagram](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>Wiring diagram showing the DC outputs from the PSUs connecting to the controller board's power inputs and the Raspberry Pi's GPIO pins.</figcaption>
</figure>