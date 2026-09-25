# Before First Power-On

Before connecting the My-Cloner to mains power for the first time, complete all checks on this page.

The goal is to confirm that the machine is mechanically complete, electrically safe and ready for its first controlled power-up.

!!! warning "Do Not Skip This Check"
    Do not connect the printer to mains power until all mechanical and electrical checks have been completed.

---

## Mechanical Check

Confirm that the printer assembly is complete and that no parts are loose or obstructed.

Check the following:

- All structural screws are installed and tightened.
- The frame is stable and does not rock.
- The X-axis moves freely from left to right.
- The Y-axis moves freely forwards and backwards.
- The Z-axis gantry can move vertically without binding.
- Both Z lead screws rotate freely.
- The belts are installed correctly.
- The belts are tensioned but not excessively tight.
- The extruder carriage moves freely.
- The heated bed moves freely along the full Y-axis travel.
- No cables interfere with moving parts.
- No tools, screws, washers or loose parts remain inside the printer.

!!! tip "Move the Axes by Hand"
    With the printer powered off, gently move the X and Y axes by hand.

    Movement should be smooth and should not require excessive force.

---

## Heated Bed and Print Surface

Check the print bed assembly before powering the machine.

Confirm that:

- The heated bed is securely mounted.
- The bed wiring is not under tension.
- The bed cables can move freely throughout the full Y-axis travel.
- The magnetic surface is correctly installed.
- The spring steel sheet sits flat on the bed.
- The PEI surface is clean.
- Any protective shipping film has been removed, if applicable.

Do not place tools or other objects on the print surface before the first homing procedure.

---

## Hotend and Extruder Check

Inspect the complete extruder and hotend assembly.

Confirm that:

- The hotend is securely mounted.
- The nozzle is installed correctly.
- The heater cartridge is secured inside the heater block.
- The thermistor is secured correctly.
- The hotend fan is installed.
- The part-cooling fan is installed.
- Fan cables cannot contact the heater block or nozzle.
- The extruder motor is securely mounted.
- The filament path is unobstructed.

!!! warning "Heater and Thermistor"
    A loose heater cartridge or thermistor can cause unsafe temperature readings or uncontrolled heating.

    Do not power the printer if either component is loose or damaged.

---

## Z Probe Check

The My-Cloner Rev A uses a **P.I.N.D.A. probe**.

Before first power-on, confirm that:

- The probe is securely mounted.
- The probe body is not damaged.
- The probe cable is routed safely.
- The cable does not interfere with X-axis movement.
- The probe is positioned close to the nozzle height, according to the assembly instructions.

Do not perform automatic Z homing until the probe installation has been verified.

---

## Filament Sensor Check

Check the filament sensor assembly.

Confirm that:

- The sensor is securely installed.
- The mechanical ball and magnet mechanism moves freely.
- The filament path is unobstructed.
- The sensor cable is correctly routed.
- The cable cannot contact moving or hot components.

---

## Wiring Check

Inspect all low-voltage wiring before connecting mains power.

Check every connection individually.

Confirm that:

- All connectors are fully inserted.
- No connector is installed at an angle.
- No wires are loose inside screw terminals.
- No bare copper is exposed outside terminals.
- No wires are crushed by printed parts or frame components.
- Cables are secured away from belts, rods, lead screws and fans.
- Cable movement does not restrict any axis.

Pay particular attention to:

- Mainboard power input
- Heated bed power
- Hotend heater
- Hotend thermistor
- Bed thermistor
- Hotend fan
- Part-cooling fan
- Stepper motors
- P.I.N.D.A. probe
- Filament sensor
- Raspberry Pi power wiring
- LM2596 DC-DC converter

---

## Check 24 V Polarity

The My-Cloner uses a **24 V DC electrical system**.

Before power-up, verify the polarity of every DC power connection.

Check that:

- Positive (+) terminals are connected to positive wiring.
- Negative (-) terminals are connected to negative wiring.
- The MKS Robin Nano V3 receives the correct polarity.
- The heated bed receives the correct polarity.
- The LM2596 input receives 24 V with the correct polarity.
- The LM2596 output is connected correctly to the Raspberry Pi power input.

!!! danger "Reverse Polarity"
    Reverse polarity can permanently damage the mainboard, Raspberry Pi, DC-DC converter and other electronics.

    Do not rely only on wire colour. Verify the actual connection path.

---

## LM2596 Output Check

The Raspberry Pi Zero 2 W is powered through an **LM2596 DC-DC converter**.

Before connecting the LM2596 output to the Raspberry Pi, verify the converter output voltage.

The output must be set to approximately:

**5 V DC**

!!! danger "Check Before Connecting the Raspberry Pi"
    Do not connect the Raspberry Pi to an unverified LM2596 output.

    An output voltage significantly above 5 V can damage the Raspberry Pi.

If the converter has not yet been adjusted, disconnect its output from the Raspberry Pi before the first electrical test.

---

## Mainboard Check

Inspect the **MKS Robin Nano V3**.

Confirm that:

- The board is securely mounted.
- The board cannot contact conductive parts of the frame.
- Power wiring is correctly connected.
- Stepper motor connectors are correctly installed.
- Heater and fan connections are secure.
- Temperature sensors are connected.
- The P.I.N.D.A. probe is connected to the intended input.
- The filament sensor is connected correctly.
- No loose screws or metal objects are near the board.

---

## Raspberry Pi Check

Inspect the **Raspberry Pi Zero 2 W** installation.

Confirm that:

- The Raspberry Pi is securely mounted.
- The board cannot contact the metal frame.
- The power connection is correct.
- The connection between the Raspberry Pi and the MKS Robin Nano V3 is installed correctly.
- No cable is under mechanical stress.

---

## AC Input Check

The My-Cloner uses an IEC C14 mains inlet with an integrated switch and fuse.

Before connecting the printer to the wall outlet, confirm that:

- The IEC inlet is securely installed.
- The power switch operates correctly.
- A suitable fuse is installed.
- Live, neutral and protective earth conductors are correctly connected.
- No mains conductor is exposed.
- All mains connections are mechanically secure.
- Protective earth is connected where required.
- Mains wiring is physically separated from low-voltage wiring where possible.

!!! danger "Mains Voltage"
    AC mains voltage can cause serious injury or death.

    Never work on mains wiring while the printer is connected to the power outlet.

    If you are not qualified or confident working with mains voltage, have this section inspected by a qualified person.

---

## Power Supply Check

The My-Cloner Rev A uses a:

**Mean Well LRS-350-24**

Before connecting the printer to mains power, inspect the power supply carefully.

Confirm that:

- The PSU is securely mounted.
- AC input wiring is correctly connected.
- Protective earth is connected correctly.
- 24 V output wiring is correctly connected.
- Terminal screws are tight.
- No exposed conductor can contact the PSU enclosure.
- Ventilation openings are not blocked.

### Input Voltage Selector

The Mean Well LRS-350-24 includes an input voltage selector.

For operation on a 230 V mains supply, the selector must be set to the appropriate 230 V position.

!!! danger "Verify the Voltage Selector"
    Check the PSU voltage selector before connecting the printer to mains power.

    An incorrect selector position may damage the power supply and connected electronics.

---

## Fuse Check

Verify that the fuse installed in the IEC inlet matches the electrical design of the My-Cloner Rev A.

Check that:

- The fuse is installed.
- The fuse holder closes correctly.
- The fuse is not visibly damaged.
- The fuse rating matches the documented electrical specification.

Do not replace the fuse with a higher-rated fuse simply to prevent it from blowing.

A blown fuse indicates that the cause should be investigated.

---

## Cable Management Check

Before first power-on, move every axis through its available travel by hand and observe the cables.

Confirm that:

- No cable becomes tight.
- No cable is pulled from a connector.
- No cable enters a fan.
- No cable touches the hotend.
- No cable rubs against sharp edges.
- No cable interferes with belts or lead screws.

Cable movement should remain controlled throughout the full motion range.

---

## Final Visual Inspection

Perform one complete visual inspection of the printer.

Look for:

- Loose screws
- Loose connectors
- Exposed copper
- Damaged insulation
- Pinched wires
- Foreign metal objects
- Missing components
- Incorrect connector orientation
- Tools left inside the printer
- Anything that could obstruct movement

If something looks uncertain, correct it before continuing.

---

## Pre-Power Checklist

Complete this checklist before connecting mains power.

- [ ] Frame and mechanical assemblies are secure.
- [ ] X-axis moves freely.
- [ ] Y-axis moves freely.
- [ ] Z-axis moves freely.
- [ ] Belts are installed and tensioned correctly.
- [ ] Heated bed and spring steel sheet are correctly installed.
- [ ] Hotend and extruder are secure.
- [ ] P.I.N.D.A. probe is correctly installed.
- [ ] Filament sensor is correctly installed.
- [ ] All low-voltage wiring has been checked.
- [ ] 24 V polarity has been verified.
- [ ] LM2596 output has been set and verified at approximately 5 V.
- [ ] MKS Robin Nano V3 connections have been checked.
- [ ] Raspberry Pi Zero 2 W installation has been checked.
- [ ] IEC inlet wiring has been checked.
- [ ] Protective earth connections have been checked.
- [ ] PSU wiring has been checked.
- [ ] PSU input voltage selector has been verified.
- [ ] Fuse is installed and correctly rated.
- [ ] Cable movement has been checked across all axes.
- [ ] No loose parts or tools remain inside the printer.

---

!!! success "Pre-Power Check Complete"
    If every item above has been verified, the My-Cloner is ready for its first controlled power-on.

Continue with:

[First Power-On](first-power-on.md)