# Replacing the Heater Cartridge

The heater cartridge is the component inside the heater block responsible for melting the filament. If your hotend fails to heat up, and you've confirmed the wiring is correct, the cartridge itself may have failed.

!!! danger "Safety First: Cool Down and Unplug"
    Ensure the printer is off and completely cool before handling hotend components.

### Procedure

1.  **Access the Heater Block**: Remove the toolhead shroud and any silicone sock to get clear access to the heater block.

2.  **Disconnect Old Heater**: Trace the two wires from the heater cartridge to their connector and disconnect them.

3.  **Remove Old Heater Cartridge**: Locate the small grub screw on the heater block that clamps the cartridge in place. Loosen this screw. The old cartridge should now slide out. It may be a snug fit and require a gentle pull with pliers.

<figure markdown="1">
  ![Locating the heater cartridge grub screw](/images/image-placeholder.png#only-light){ width="600" }
  ![Locating the heater cartridge grub screw](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A close-up of the heater block with an arrow pointing to the small grub screw used to secure the heater cartridge.</figcaption>
</figure>

4.  **Insert New Heater Cartridge**: Slide the new cartridge fully into the hole in the heater block.

5.  **Secure New Cartridge**: Gently tighten the grub screw. It should be snug enough to hold the cartridge firmly so it cannot slide out, but **do not overtighten**, as this can deform the cartridge and create heating issues.

6.  **Reconnect and Reassemble**: Reconnect the new heater wires and re-assemble the toolhead.

!!! warning "You MUST PID Tune After Replacement"
    Every heater cartridge has slightly different heating properties. After replacing it, you **must** perform a PID tune of the hotend to ensure stable and accurate temperature control.