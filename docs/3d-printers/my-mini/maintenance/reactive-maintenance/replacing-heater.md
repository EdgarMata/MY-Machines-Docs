# Replacing the Heater Cartridge

The heater cartridge is responsible for heating the hotend to the correct printing temperature. If your printer is having trouble reaching or maintaining temperature, you may need to replace the heater cartridge. This guide will show you how to do it on your **MY-Mini 3D Printer**.

---

## Tools Required
- Hex key set
- Small screwdriver (for the mainboard terminals)
- Pliers
- Wire cutters
- Zip ties

---

## Safety First

- **Turn off and unplug the printer:** This is the most important step. Ensure the printer is completely disconnected from power.
- **Let the hotend cool down:** The hotend can cause severe burns. Make sure it is at room temperature before you begin.

---

## Procedure

### 1. **Access the Hotend**
1.  You will need to remove the print head cover or shroud to get to the hotend assembly. This is usually held on by a few screws.
2.  Take pictures as you go to help with reassembly.

### 2. **Disconnect the Old Heater Cartridge**
1.  Trace the wires from the heater cartridge back to the mainboard.
2.  You may need to open the electronics enclosure to access the mainboard.
3.  The heater wires are usually thick and are screwed into a terminal block on the mainboard. Loosen the screws and remove the wires.
4.  Carefully cut any zip ties and unroute the heater wires from the print head back to the mainboard.

### 3. **Remove the Old Heater Cartridge**
1.  The heater cartridge is a small metal cylinder inserted into the heater block.
2.  It is usually held in place by a small grub screw on the heater block.
3.  Use the correct size hex key to loosen this screw. You do not need to remove it completely.
4.  Once the screw is loose, you should be able to slide the heater cartridge out of the heater block. It may be a tight fit, so you might need to gently wiggle it with pliers.

### 4. **Install the New Heater Cartridge**
1.  Slide the new heater cartridge into the heater block. Make sure it is inserted fully.
2.  Tighten the grub screw to secure the new cartridge in place. It should be snug, but do not overtighten as this can damage the cartridge.
3.  Route the new heater wires back to the mainboard, following the same path as the old ones.
4.  Insert the wires into the correct terminal block on the mainboard and tighten the screws. Heater cartridges are not polarized, so it doesn't matter which wire goes into which terminal.

### 5. **Reassemble and Test**
1.  Tidy up the wiring and use new zip ties to secure it.
2.  Reattach the print head cover and any other parts you removed.
3.  Plug in and turn on the printer.
4.  **PID Tune:** This is a very important step. The new heater may have slightly different properties than the old one. You must run a PID tune to ensure stable temperatures. You can do this by sending the command `M303 E0 S215 C8` to your printer via a terminal, then saving the results with `M500`.
5.  After the PID tune, set the hotend to a target temperature and verify that it heats up and holds the temperature steadily.

---

By following these steps, you can safely replace the heater cartridge on your **MY-Mini 3D Printer**.
