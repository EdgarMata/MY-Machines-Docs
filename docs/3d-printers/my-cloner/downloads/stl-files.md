# STL Files

Download the official 3D printable parts for the **My-Cloner Rev A**.

The files in this section correspond to the printed parts listed in the current Bill of Materials.

!!! info "Use the Correct Hardware Revision"
    Always use STL files that match the hardware revision of your printer.

    The files provided on this page are intended for:

    **My-Cloner — Hardware Rev A**

## Download STL Files

The complete My-Cloner Rev A printable parts package is available as a ZIP archive.

[:material-download: Download My-Cloner Rev A STL Files](/assets/downloads/cloner/my-cloner-stls.zip){ .md-button .md-button--primary }

The archive contains the STL files required to print the My-Cloner Rev A components.

!!! note "Official Project Files"
    Use the STL files provided with the current My-Cloner release.

    Avoid mixing parts from older prototypes, inherited MK3S designs or previous revisions unless compatibility has been explicitly confirmed.

## Printed Parts

The My-Cloner Rev A includes printed components for:

- Extruder and hotend assembly
- X-axis components
- Y-axis components
- Z-axis components
- LCD mounting
- Electronics enclosure
- PSU cover
- Cable management
- Sensor mounting

For the complete list of required printed parts and quantities, see:

[Printed Parts BOM](../bom/printed-parts.md)

## Recommended Printing Settings

The following settings are a general starting point for My-Cloner printed parts:

| Setting | Recommendation |
|---|---|
| Perimeters | 4 |
| Layer Height | 0.20–0.30 mm |
| Infill | 25% |
| Material | PETG, ASA or ABS |
| Supports | As specified for each part |

These values may be adjusted according to your printer, material and slicer profile.

!!! tip "Recommended Material"
    PETG is a practical choice for most My-Cloner structural printed parts.

    ASA or ABS may also be used when higher temperature resistance is required.

## Before Printing

Before starting a complete set of parts:

1. Confirm that the files belong to the My-Cloner Rev A.
2. Verify the quantity of each part against the BOM.
3. Check for left and right variants.
4. Inspect the model orientation in the slicer.
5. Preview the generated toolpaths before printing.
6. Confirm that the selected material is suitable for the component.

Pay particular attention to paired parts such as:

- LCD Support (L) / LCD Support (R)
- Z Axis Top (L) / Z Axis Top (R)
- Z Motor Mount (L) / Z Motor Mount (R)

## File Formats

The primary printable format is:

**STL**

The files are distributed as a ZIP archive for easier downloading and storage.

Additional source CAD formats may be available separately in:

[CAD Files](cad-files.md)

STL files are intended for slicing and printing. Use the CAD source files when you need to inspect or modify the original geometry.

## Slicing

The recommended slicer for the My-Cloner is:

**OrcaSlicer**

MyMachines slicer profiles are available in:

[Slicer Profiles](slicer-profiles.md)

You may also use another compatible slicer if you prefer.

## File Integrity

Before printing:

- Confirm that the STL imports without errors.
- Check that the model dimensions appear correct.
- Inspect thin walls and small features.
- Verify that no geometry is missing.
- Confirm that the part sits correctly on the build plate.

Do not print a complete set if a file appears damaged or incompatible with the current revision.

## Related Documentation

For the required quantities and part names:

[Printed Parts BOM](../bom/printed-parts.md)

For editable engineering files:

[CAD Files](cad-files.md)

For recommended slicing profiles:

[Slicer Profiles](slicer-profiles.md)

Once the printed parts are ready, continue with:

[Assembly Guide](../assembly/01_introduction.md)