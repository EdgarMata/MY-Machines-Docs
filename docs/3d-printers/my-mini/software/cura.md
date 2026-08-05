# Cura Setup for MY-Mini

Ultimaker Cura is another excellent, free, and popular slicer that is fully compatible with your **MY-Mini 3D Printer**. Its user-friendly interface makes it a great choice for both beginners and advanced users. This guide will help you set it up.

---

## 1. Setting Up the Printer Profile

Cura doesn't have a pre-made profile for the MY-Mini, so you'll need to add it as a custom printer.

1.  Open Cura. Go to `Settings` > `Printer` > `Add Printer`.
2.  Select `Add a non-networked printer`.
3.  Scroll down and select `Custom` > `Custom FFF printer`. Click `Add`.
4.  In the "Machine Settings" window, configure the printer's dimensions:
    *   **X (Width):** 180 mm
    *   **Y (Depth):** 180 mm
    *   **Z (Height):** 180 mm
    *   **Build Plate Shape:** Rectangular
    *   **Origin at center:** Unchecked (This assumes the origin is at the front-left corner).
    *   **Heated Bed:** Checked
5.  Go to the `Extruder 1` tab:
    *   **Nozzle Size:** 0.4 mm
    *   **Compatible material diameter:** 1.75 mm
6.  Click `Finish`. You now have a profile for your MY-Mini.

---

## 2. Understanding Profiles in Cura

Cura uses profiles to manage settings. You can select a default profile (e.g., "Standard Quality") and then customize it. Your changes can be saved as a new custom profile.

-   **Print Settings:** The main panel on the right allows you to adjust everything from layer height to infill and supports. You can select the level of setting visibility from `Basic` to `All`.
-   **Filament and Printer:** At the top of the settings panel, you can confirm your printer and the type of material you are using (e.g., Generic PLA). Selecting the correct material type will apply a good baseline of temperature and retraction settings.

---

## 3. Recommended Print Settings

Here are good starting points for common filaments. You can adjust these in the "Print Settings" panel.

### PLA
-   **Printing Temperature:** 210-220 °C
-   **Build Plate Temperature:** 60 °C
-   **Speed:** `50 mm/s` is a good all-around speed.
-   **Retraction:** Enabled. For a direct drive, start with `1mm` Distance and `35 mm/s` Speed.
-   **Cooling:** Enable Print Cooling, with the fan at 100% after the first few layers.

### PETG
-   **Printing Temperature:** 230-250 °C
-   **Build Plate Temperature:** 70-85 °C
-   **Speed:** `40 mm/s` can help reduce stringing.
-   **Retraction:** Enabled. You may need to fine-tune these settings. Try `1.5mm` at `40 mm/s`.
-   **Cooling:** Reduce fan speed to `30-50%` to improve layer strength.

### ABS
-   **Printing Temperature:** 240-260 °C
-   **Build Plate Temperature:** 95-110 °C
-   **Speed:** `40-50 mm/s`.
-   **Cooling:** Disable Print Cooling (set fan speed to 0%).
-   **Enclosure:** An enclosure is highly recommended to prevent warping.

---

## 4. Bed Adhesion and Supports

-   **Build Plate Adhesion:**
    *   A **Skirt** (the default) just primes the nozzle.
    *   A **Brim** is recommended for parts with a small base or sharp corners to prevent them from lifting off the bed.
    *   A **Raft** can be used for very difficult-to-stick materials or parts with a very complex base.
-   **Generate Support:**
    *   Check this box to enable supports for overhangs.
    *   **Support Structure:** `Normal` supports are standard, but `Tree` supports are excellent as they use less material and are often easier to remove.
    - **Support Placement:** `Touching Buildplate` is usually sufficient, but `Everywhere` will support features on top of your model.
