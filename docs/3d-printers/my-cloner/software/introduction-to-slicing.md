# Introduction to Slicing Software

Before your 3D printer can bring a digital model to life, that model must be translated into a language the printer can understand. This is the job of a **Slicer**.

!!! info "What is a Slicer?"
    A Slicer is a piece of software on your computer that converts a 3D model file (like a `.stl` or `.step` file) into a detailed, layer-by-layer instruction file called **G-code**. This G-code file tells the printer exactly where to move, how fast to go, and how much plastic to extrude at every single point of the print.

---
### Our Recommended Slicer: Orca Slicer

While there are many great slicers available, we recommend **Orca Slicer** for the MY Cloner 3D Printer.

* **Why Orca Slicer?**
    * It's a modern, powerful, and easy-to-use slicer based on the excellent foundations of PrusaSlicer and Bambu Studio.
    * It has outstanding built-in integration for printers running **Klipper firmware**.
    * Its "Device" tab allows you to connect directly to your printer over the network to upload files, monitor print progress, and control the machine, creating a seamless workflow.

### Support for Other Slicers

We understand that you may have a preference for other popular slicers. Because of this, we also provide tested profiles for **PrusaSlicer** and **SuperSlicer**. The setup process for these is covered in a separate guide in this section.

### The Basic Slicing Workflow

No matter which slicer you use, the basic process is always the same:

1.  **Import Model:** Open your 3D model file in the slicer.
2.  **Select Profiles:** Choose your printer, filament, and desired print quality.
3.  **Slice & Preview:** The software calculates the toolpaths for every layer. You can then preview the result to ensure everything looks correct.
4.  **Upload & Print:** Send the generated G-code file to the printer.