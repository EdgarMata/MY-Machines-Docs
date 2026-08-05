# PrusaSlicer Setup for MY-Mini

PrusaSlicer is a powerful, open-source slicer that is highly recommended for your **MY-Mini 3D Printer**. It's known for its advanced features, regular updates, and excellent print quality. This guide will walk you through setting it up for your printer.

---

## 1. Setting Up the Printer Profile

First, you need to tell PrusaSlicer about your printer's hardware.

1.  Open PrusaSlicer and run the Configuration Wizard (`Configuration` > `Configuration Wizard`).
2.  On the "Prusa FFF" page, you can uncheck all printers.
3.  On the "Other Vendors" page, select `Custom Printer`.
4.  On the next screen, define your printer's profile:
    *   **Firmware Type:** `Marlin (Legacy)`
    *   **Bed Shape:** Set the dimensions to **180 x 180 mm**. The origin should be at the front-left corner, so set it to **X: 0, Y: 0**.
    *   **Printable Height (Z):** Set to **180 mm**.
    *   **Nozzle Diameter:** `0.4 mm` (or your installed nozzle size).
    *   **Extruder Temperature:** `215 °C` (for PLA, can be changed later).
    *   **Bed Temperature:** `60 °C` (for PLA, can be changed later).
5.  Click `Finish`. You now have a basic profile for your MY-Mini.

---

## 2. Understanding Profiles

PrusaSlicer organizes settings into three main categories:

-   **Print Settings:** Controls the quality and speed of the print (layer height, infill, supports, etc.). You can have multiple print profiles (e.g., "0.15mm Quality", "0.25mm Draft").
-   **Filament Settings:** Controls filament-specific properties (temperatures, cooling, retraction). You should have a profile for each type and brand of filament you use (e.g., "MyBrand PLA", "Generic PETG").
-   **Printer Settings:** Defines the hardware of your printer. You will generally only have one profile here for your MY-Mini.

---

## 3. Recommended Filament Settings

Here are good starting points for common filaments. You should create a new filament profile for each.

### PLA
-   **Extruder Temperature:** 210-220 °C
-   **Bed Temperature:** 60 °C
-   **Cooling:** 100% fan speed after the first few layers.
-   **Retraction:** A good starting point is `0.8mm` distance at `35 mm/s` speed for a direct drive extruder.

### PETG
-   **Extruder Temperature:** 230-250 °C
-   **Bed Temperature:** 70-85 °C
-   **Cooling:** 30-50% fan speed. Too much cooling can cause poor layer adhesion.
-   **Retraction:** PETG is prone to stringing. Try `1.0mm` distance at `40 mm/s` and consider increasing Z-hop.

### ABS
-   **Extruder Temperature:** 240-260 °C
-   **Bed Temperature:** 95-110 °C
-   **Cooling:** Turn the part cooling fan off (0-10%). ABS needs to cool slowly to prevent warping and cracking.
-   **Enclosure:** An enclosure is highly recommended to maintain a stable ambient temperature.

---

## 4. Print Quality and Speed

-   **Layer Height:** For detailed prints, use `0.15mm`. For faster drafts, use `0.20mm` or `0.25mm`.
-   **First Layer Height:** A thicker first layer, like `0.20mm`, can improve bed adhesion.
-   **Infill:** `15-20%` with the `Grid` or `Gyroid` pattern is a good all-around choice.
-   **Speed:** A general print speed of `40-50 mm/s` for perimeters and `60-80 mm/s` for infill is a good starting point.

---

## 5. Supports and Bed Adhesion

-   **Bed Adhesion:** For parts with a small footprint or sharp corners, use a **Brim** of `3-5mm` to prevent warping and improve adhesion.
-   **Supports:** PrusaSlicer has excellent support options. For most models, `Grid` supports work well. For complex organic shapes, try **Tree supports** (`Paint-on supports` > `Style` > `Organic`). Set the overhang threshold to around `45 degrees`.
