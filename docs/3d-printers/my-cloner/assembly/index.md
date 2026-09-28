# My-Cloner Assembly Guide

This section describes the mechanical and electrical assembly of the **My-Cloner Rev A**.

The guide is organized in the same general order in which the machine is built, beginning with preparation and the mechanical axes, followed by the toolhead, display, heated bed, power system and electronics.

The assembly documentation is based on the current My-Cloner Rev A design, BOM and electrical architecture.

!!! important "Rev A Documentation"
    The instructions in this section apply to the My-Cloner Rev A.

    Do not assume that assembly instructions, dimensions or component choices from earlier My-Cloner prototypes or other printer designs apply to this revision.

---

## Before You Begin

Before starting the build:

- Review the current [Bill of Materials](../bom/index.md)
- Make sure all required mechanical and electronic components are available
- Prepare the required tools
- Print the required parts
- Work on a clean and stable surface
- Keep electronic components protected from electrostatic discharge until needed
- Read each assembly section before carrying out the procedure

Safety information specific to a particular assembly operation will be shown directly where it is relevant.

For normal operating safety after assembly, see the [Safety](../safety/index.md) section.

---

## Assembly Sequence

<div class="grid cards" markdown>

-   :material-tools:{ .lg .middle } **Introduction & Preparation**

    ---

    Prepare the workspace, tools, components and printed parts before beginning the build.

    [:octicons-arrow-right-24: Start Here](01_introduction.md)

-   :material-axis-y-arrow:{ .lg .middle } **Y-Axis Assembly**

    ---

    Assemble the main frame, Y carriage, linear motion system, motor and belt drive.

    [:octicons-arrow-right-24: Y-Axis Assembly](02_y-axis_assembly.md)

-   :material-axis-x-arrow:{ .lg .middle } **X-Axis Assembly**

    ---

    Assemble the X-axis end parts, smooth rods, bearings, motor and belt-tensioning hardware.

    [:octicons-arrow-right-24: X-Axis Assembly](03_x-axis_assembly.md)

-   :material-arrow-up-down:{ .lg .middle } **Z-Axis Assembly**

    ---

    Install the dual Z motors, lead screws, smooth rods and X-axis gantry.

    [:octicons-arrow-right-24: Z-Axis Assembly](04_z-axis_assembly.md)

-   :material-printer-3d-nozzle:{ .lg .middle } **Extruder Assembly**

    ---

    Assemble the direct-drive extruder, hotend, filament sensor, cooling system and P.I.N.D.A. V1.

    [:octicons-arrow-right-24: Extruder Assembly](05_e-axis_assembly.md)

-   :material-monitor:{ .lg .middle } **Display Assembly**

    ---

    Install the My-Cloner Rev A local display hardware.

    [:octicons-arrow-right-24: Display Assembly](06_lcd_assembly.md)

-   :material-radiator:{ .lg .middle } **Heated Bed & Power Supply**

    ---

    Install the heated bed and main power-supply hardware.

    [:octicons-arrow-right-24: Heated Bed & Power Supply](07_heatbed_and_psu_assembly.md)

-   :material-expansion-card:{ .lg .middle } **Electronics Assembly**

    ---

    Install the controller, Raspberry Pi power system, drivers and remaining electronic hardware.

    [:octicons-arrow-right-24: Electronics Assembly](08_electronics_assembly.md)

-   :material-clipboard-check-outline:{ .lg .middle } **Pre-Flight Check**

    ---

    Inspect the completed assembly before beginning the controlled initial setup and power-on procedure.

    [:octicons-arrow-right-24: Pre-Flight Check](09_pre-flight_check.md)

</div>

---

## How This Guide Is Organized

The assembly chapters use descriptive sections rather than numbered steps.

For example:

    ## Y-Carriage

    ### Installing the Linear Bearings

    ### Installing the Smooth Rods

    ### Aligning the Carriage

Numbered lists are used only when a specific operation must be performed in a defined sequence.

This keeps the documentation easier to navigate and allows individual assembly procedures to be updated without renumbering the entire chapter.

---

## Images

Some assembly photographs are still being prepared.

Where a final photograph is not yet available, the guide uses a placeholder image with a caption describing the required photograph.

These captions define the view, orientation and detail that the final documentation image should show.

Example:

<figure markdown="1">
  ![Assembly Photo Placeholder](/assets/images/image-placeholder.webp#only-light){ width="610" }
  ![Assembly Photo Placeholder](/assets/images/image-placeholder.webp#only-dark){ width="610" }
  <figcaption>Photo required: clear front-left view of the assembly showing the installed component, its orientation and the relevant fasteners.</figcaption>
</figure>

---

## Documentation Sources

The assembly guide should be read together with:

- [Bill of Materials](../bom/index.md) — required parts and specifications
- [Wiring & Electronics](../wiring/index.md) — electrical connections and hardware assignments
- [Safety](../safety/index.md) — safe operation of the completed machine
- [Initial Setup](../operation/initial-setup/) — commissioning and first power-on procedures

Mechanical dimensions, fasteners and component assignments must match the current Rev A BOM and CAD model.

Electrical connections must match the current wiring documentation and electrical schematic.