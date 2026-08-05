# Initial Setup

This section will guide you through the first steps after assembling your MY-Mini-3D-Printer, with recommendations inspired by the Prusa Mini.

## 1. Firmware Installation
- Marlin is recommended, compatible with the MKS SGEN_L V2.0.
- Download the latest version of Marlin and configure it for your hardware (TMC2209 drivers, MKS H43 display, P.I.N.D.A. sensor, etc).
- Flash the firmware to the board via USB.
- See the official Makerbase and Marlin documentation for configuration details.

## 2. Display and Driver Configuration
- Ensure the MKS H43 display is properly connected to the board.
- Configure the TMC2209 drivers for UART (silent) mode and adjust current as needed for the motors.

## 3. Bed Leveling (Mesh Bed Leveling)
- Use the P.I.N.D.A. sensor for automatic bed leveling.
- In the display menu, select "Auto Home" and then "Bed Leveling".
- Follow the instructions to ensure the first layer adheres correctly.

## 4. Motor and Sensor Testing
- In the control menu, test the movement of the X, Y, and Z axes.
- Check if the endstops are working correctly.
- Test the hotend and bed heating.

## 5. First Test Print
- It is recommended to print a calibration cube (20x20x20mm) to validate operation.
- Adjust the Z-offset if necessary.

## Prusa Mini Tips
- Use Prusa Mini slicer profiles as a base for the MY-Mini.
- Enable "mesh bed leveling" to ensure first layer quality.
- Check Prusa user forums and groups for configuration tips.

> For questions, see the troubleshooting section or share in the My Machines community.
