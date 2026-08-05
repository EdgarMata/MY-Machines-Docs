# Glossary of Common 3D Printing Terms

This glossary provides simple definitions for some of the common terms you will encounter in 3D printing and in this documentation.

---
* **Bed / Heatbed:** The heated build plate where the 3D model is printed.
* **Brim:** A feature in the slicer that adds a single layer of extra material around the base of a model to help with bed adhesion and prevent warping.
* **Extruder:** The entire mechanism on the print head that draws in, melts, and pushes out the filament.
* **Filament:** The plastic material, usually on a spool, used to create 3D prints.
* **Firmware:** The software that runs on the printer's mainboard and host computer, controlling all its actions. In this case, **Klipper**.
* **G-code:** The language of 3D printers. It's a text file containing a long list of commands that tell the printer exactly where to move and what to do.
* **Host:** In a Klipper system, this is the small computer (like a Raspberry Pi) that runs the main Klipper software and the web interface.
* **Hotend:** The part of the extruder that gets hot to melt the filament. It includes the nozzle, heater block, and heatsink.
* **Klipper:** A high-performance 3D printer firmware that uses a host computer combined with the printer's mainboard (MCU) to achieve higher speeds and precision.
* **MCU (Micro-controller Unit):** The printer's main electronics board. In a Klipper system, its only job is to execute commands sent by the Host.
* **Overhang:** A part of a model that is printed over open air without any support directly below it.
* **Retraction:** The action of the extruder motor pulling the filament backward slightly to relieve pressure in the nozzle and prevent stringing.
* **Slicer:** A piece of software on your computer (e.g., PrusaSlicer, Cura) that converts a 3D model file (`.stl`) into a `.gcode` file that the printer can understand.
* **STL (`.stl`):** The most common file format for 3D models that you download from the internet or create yourself.
* **Stringing:** A print defect where fine, hair-like strands of plastic are left between different parts of a model.
* **Warping:** A print defect where the corners of a model lift off the print bed due to thermal contraction. 