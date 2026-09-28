# Pre-Flight Check

This chapter covers the final **mechanical pre-power checks** after assembly. Electrical bring-up and machine-specific validation are separate stages and must be completed before normal calibration or printing.

---
## Assembly Procedure

### Step 1: Setting the Initial Z-Probe Height

This procedure sets a rough, safe starting distance between your Z-probe and the nozzle tip. It is the most important step in this chapter.

!!! danger "Printer Must Be OFF"
    This entire procedure must be performed with the printer **turned off and unplugged** from the power outlet.

* **Action 1: Lower the Nozzle to the Bed**
    * Manually turn both Z-axis lead screws slowly and simultaneously to lower the entire X-axis gantry.
    * Continue lowering until the tip of the **nozzle just barely touches** the surface of the heated bed. Do this gently and do not press down or bend the heatbed.
    * **Important:** Do not have the flexible steel print sheet on the bed for this process.

* **Action 2: Use a Zip Tie as a Gauge**
    * Manually move the extruder to the side so you have clear access to the Z-probe.
    * Take a standard zip tie from your kit and place it flat on the bed, directly underneath the Z-probe sensor.
    * Loosen the screw that holds the Z-probe in place.
    * Let the probe rest gently on top of the zip tie.
    * While holding the probe in this position, re-tighten the screw to secure it.

!!! info "Coarse Mechanical Adjustment Only"
    This step provides only an initial mechanical relationship between the probe and nozzle.

    The final P.I.N.D.A. mounting position, electrical input and Z offset must be confirmed during the controlled Rev A bring-up. Do not assume this mechanical adjustment alone makes Z homing safe.

<figure markdown="1">
  ![Z-Probe Adjustment with Zip Tie](/assets/images/image-placeholder.webp#only-light){ width="500" }
  ![Z-Probe Adjustment with Zip Tie](/assets/images/image-placeholder.webp#only-dark){ width="500" }
  <figcaption>Illustration showing a zip tie placed under the Z-probe to set the initial height relative to the nozzle.</figcaption>
</figure>

---
### Step 2: Continue to Controlled Bring-Up

The mechanical build is now ready for the staged electrical and firmware checks.

Proceed in this order:

1. [Before First Power-On](../operation/initial-setup/before-first-power-on.md)
2. [First Power-On](../operation/initial-setup/first-power-on.md)
3. [First Time Setup & Calibration](../operation/initial-setup/first-time-setup.md)

!!! warning "Do Not Skip Bring-Up Stages"
    Do not jump directly to full homing, heater calibration or a first print.

    Rev A sensorless homing, P.I.N.D.A., thermistors, fans and other machine-specific parameters must be validated in the controlled sequence.

---
### Step 3: Where to Find Printable 3D Models

Your kit may have come with an SD card or a download link containing some pre-sliced test models that are ready for your first print, such as a calibration cube or a Benchy.

When you are ready to find more models, we recommend these popular community sites:

* [Printables.com](https://www.printables.com)
* [Thingiverse.com](https://www.thingiverse.com)
* [MyMiniFactory.com](https://www.myminifactory.com)
* [Cults3D.com](https://cults3d.com)
* [Thangs.com](https://thangs.com)
* [MakerWorld.com](https://makerworld.com/)

---
### Step 4: Getting Help and Joining the Community

If you encounter any problems during calibration or printing, we are here to help.

* First, check out our comprehensive **[Troubleshooting Section](../troubleshooting/layer-adhesion-issues.md)**.
* Join our community on [Facebook](https://www.facebook.com/mymachinescom/) to ask questions and share your creations with other users.

---
### Step 5: You've Finished the Build!

!!! success "Congratulations on Building Your 3D Printer!"
    You have successfully completed the entire assembly process. You've built a complex machine from scratch, and you should be very proud of your work.

    You are now ready to begin the controlled pre-power and bring-up procedure.

