# Replacing the Hotend

The hotend is the heart of your 3D printer, responsible for melting and extruding filament. If you have a severe clog that cannot be cleared, or if the hotend is damaged, you may need to replace the entire assembly. This guide will walk you through the process for your **MY-Mini 3D Printer**.

---

## Tools Required
- Hex key set
- Pliers
- Wire cutters
- Zip ties
- A new, complete hotend assembly for your printer model

---

## Safety First

- **Turn off and unplug the printer:** Ensure the printer is completely disconnected from power before you start.
- **Let the hotend cool down:** Make sure the hotend is at room temperature to avoid burns.

---

## Procedure

### 1. **Disassemble the Print Head**
1.  Remove the print head cover/shroud to expose the hotend.
2.  Take photos of the wiring and assembly to help you remember how it goes back together.

### 2. **Disconnect Wiring**
1.  Carefully disconnect the heater cartridge and thermistor wires from the mainboard. You will likely need to open the electronics enclosure.
2.  Disconnect the hotend cooling fan.
3.  Cut any zip ties and carefully pull the bundle of wires out of any cable sleeves and back through to the print head.

### 3. **Remove the Old Hotend**
1.  The hotend is typically mounted to the X-axis carriage with a couple of screws. Loosen these screws.
2.  The entire hotend assembly, including the heater block, heat sink, and fans, should now be free to be removed from the printer.

### 4. **Prepare the New Hotend**
1.  Unbox your new hotend. It should come pre-assembled with a heater cartridge, thermistor, and heat sink.
2.  If the fans are not pre-installed, mount them onto the new hotend now. Ensure the hotend cooling fan is pointing towards the heat sink.

### 5. **Install the New Hotend**
1.  Mount the new hotend assembly onto the X-axis carriage and secure it with the mounting screws.
2.  Route the new wiring harness back to the electronics enclosure, following the same path as the old one.
3.  Connect the new heater cartridge, thermistor, and fan wires to the mainboard. Pay close attention to the polarity of the thermistor and fan wires.

### 6. **Reassemble and Final Checks**
1.  Use new zip ties to neatly manage the cables. Make sure they are secure and will not interfere with the printer's movement.
2.  Re-install the print head cover/shroud.
3.  **Level the Bed:** Replacing the hotend will almost certainly change the Z-height of the nozzle. You must re-level your print bed and set the Z-offset before you try to print.
4.  **PID Tune:** Just like replacing a heater cartridge, you must perform a PID tune for the new hotend. Send `M303 E0 S215 C8` to the printer via a terminal, and save the new values with `M500`.
5.  Load filament and do a test print to ensure everything is working as expected.

---

Replacing the hotend can seem daunting, but by being methodical and following these steps, you can get your **MY-Mini 3D Printer** back up and running.
