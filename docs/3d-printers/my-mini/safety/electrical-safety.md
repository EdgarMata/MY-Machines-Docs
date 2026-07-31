# Electrical Safety

Operating your **MY-Mini 3D Printer** involves working with electricity. Adhering to proper electrical safety practices is essential to prevent accidents and ensure safe operation.

---

## Key Electrical Safety Guidelines

### 1. **Power Supply Unit (PSU)**
- **Never open the PSU:** The power supply contains capacitors that can hold a dangerous electrical charge long after the unit is unplugged. There are no user-serviceable parts inside.
- **Use the correct voltage:** Ensure the voltage switch on your PSU (if it has one) is set to the correct voltage for your country (e.g., 115V or 230V) before plugging it in.
- **Ensure proper ventilation:** Do not cover the PSU or block its ventilation holes. It needs to dissipate heat to operate safely.

### 2. **Wiring and Connections**
- **Inspect regularly:** Before each use, give the power cord and all visible wiring a quick check for any signs of damage, fraying, or wear.
- **Secure connections:** Ensure all connectors are fully seated and that screw terminals on the mainboard are snug. Loose connections can cause heat buildup and are a fire hazard.
- **Proper grounding:** Always plug your printer into a properly grounded (earthed) outlet. This is a critical safety feature that protects you from electric shock.

### 3. **General Operation**
- **Keep liquids away:** Never place drinks or any other liquids on or near your printer.
- **Power off for maintenance:** Always turn off and unplug the printer from the wall outlet before performing any maintenance, cleaning, or modifications.

---

## Thermal Safety

Your printer has components that get extremely hot. 

- **Hotend and Nozzle:** Can reach temperatures over 250°C (482°F).
- **Print Bed:** Can reach temperatures over 100°C (212°F).

Always be aware of these hot parts during and after printing. Allow them to cool down completely before touching them.

---

## Thermal Runaway Protection

Your printer's firmware should have **Thermal Runaway Protection** enabled. This is a safety feature that automatically shuts down the printer if it detects that the hotend or bed is heating uncontrollably. You can test if it's enabled by sending the `M605 S1` command to your printer.

By following these guidelines, you can significantly reduce the risk of electrical hazards and ensure a safe printing experience with your **MY-Mini 3D Printer**.
