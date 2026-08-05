# Glossary of Terms

The world of 3D printing and Klipper is full of specific terminology. This page serves as a quick reference for some of the common terms you will encounter. 

* **Klipper**: The high-performance 3D printer firmware that runs on your machine. It uses a powerful host computer (like a Raspberry Pi) paired with a simple microcontroller (MCU).
* **MCU (Micro-controller Unit)**: The main electronics board in your printer (e.g., BTT Octopus). It receives commands from the Klipper host and controls the motors, heaters, and sensors.
* **Host**: The computer that runs the main Klipper software (in this case, your Raspberry Pi).
* **Mainsail / Fluidd**: The web interface you use to interact with and control your Klipper-powered printer.
* **`printer.cfg`**: The main configuration file for Klipper. All your printer's hardware settings, pinouts, and macros are defined here.
* **Input Shaper**: A key Klipper feature that measures and cancels out resonant frequencies in your printer, dramatically reducing "ringing" or "ghosting" artifacts for cleaner prints at high speeds.
* **Pressure Advance**: A Klipper feature that regulates extruder pressure to produce sharper corners and reduce blobbing or stringing.
* **CoreXY**: The motion system your printer uses, where two stationary motors control the toolhead's XY position through a specific belt arrangement.
* **PID Tuning**: A calibration process that fine-tunes your printer's heater control, allowing it to hold a target temperature more stably without over- or under-shooting.
* **G-Code**: The command language that 3D printers understand. It's a series of instructions that tell the printer where to move, how fast, and how much to extrude.
* **Slicer**: The software (e.g., PrusaSlicer, OrcaSlicer) that converts a 3D model (STL file) into the G-code that the printer can execute.