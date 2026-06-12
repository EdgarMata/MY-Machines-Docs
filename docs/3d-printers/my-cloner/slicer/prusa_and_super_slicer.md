# Using PrusaSlicer & SuperSlicer Profiles

While we recommend Orca Slicer for its excellent Klipper integration, we understand that you may be more comfortable with or prefer to use **PrusaSlicer** or **SuperSlicer**. We provide optimized profiles for these slicers as well.

---
### How to Import the Profiles

The process is simple and very similar to the Orca Slicer setup.

1.  Open PrusaSlicer or SuperSlicer.
2.  Go to the top menu: `File -> Import -> Import Config Bundle...`.
3.  Navigate to and select the `.ini` profile bundle file provided for your chosen slicer.
4.  The slicer will confirm the profiles to be imported. Ensure the "MY Cloner" printer profile, along with the associated filament and print profiles, are selected.
5.  Click "Import."

You should now see the "MY Cloner 3D Printer" as a selectable option in the printer dropdown menu.

!!! info "The Basic Workflow is the Same"
    Once the profiles are loaded, the day-to-day slicing workflow is nearly identical to the one described in the `Basic Slicing Workflow` guide. You will still:
    
    1.  Add a model.
    2.  Select the Printer, Filament, and Quality profiles.
    3.  Slice the model and preview the result.

---
### Key Difference: Uploading to Klipper

The main difference when using PrusaSlicer or SuperSlicer is the lack of a built-in "Device" tab for direct Klipper communication.

* After you click "Slice," you will need to use the **"Export G-code"** button to save the file to your computer.
* You must then open your printer's web interface (Mainsail/Fluidd) in your browser and upload the G-code file manually to the "G-Code Files" section before you can start the print.