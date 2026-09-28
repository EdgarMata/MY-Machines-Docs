# My-Cloner 3D Printer

![My-Cloner](/assets/images/cloner/my-cloner_01.webp){ width="1000" }

Welcome to the official documentation for the **My-Cloner Rev A**.

My-Cloner is an open-source Cartesian 3D printer project developed by MyMachines. This documentation is intended to provide the information required to understand, source, assemble, wire, configure, operate and maintain the machine.

!!! warning "Rev A — Active Validation"
    The Rev A mechanical definition and BOM are established, while several electrical and firmware parameters are still moving through physical bring-up.

    Items that require machine testing are clearly marked as **Pending validation** rather than being presented as finished specifications.

<div class="grid cards" markdown>

-   :material-format-list-checks:{ .lg .middle } **Bill of Materials**

    ---

    Review the current Rev A mechanical, electronic and printed parts.

    [:octicons-arrow-right-24: Bill of Materials](bom/index.md)

-   :fontawesome-solid-screwdriver-wrench:{ .lg .middle } **Assembly**

    ---

    Build the mechanical structure and install the Rev A electronics.

    [:octicons-arrow-right-24: Assembly Guide](assembly/01_introduction.md)

-   :material-electric-switch:{ .lg .middle } **Wiring & Electronics**

    ---

    Understand the 24 V architecture, Robin Nano V3, TMC2209 drivers, sensors and interfaces.

    [:octicons-arrow-right-24: Wiring & Electronics](wiring/index.md)

-   :fontawesome-solid-book-open:{ .lg .middle } **Operation & Setup**

    ---

    Follow the first-power, calibration and operating procedures.

    [:octicons-arrow-right-24: Operation & Use](operation/index.md)

-   :fontawesome-brands-app-store:{ .lg .middle } **Software**

    ---

    Configure the software workflow around Klipper, Mainsail and OrcaSlicer.

    [:octicons-arrow-right-24: Software](software/index.md)

-   :fontawesome-solid-screwdriver-wrench:{ .lg .middle } **Maintenance**

    ---

    Keep the machine mechanically and electrically reliable.

    [:octicons-arrow-right-24: Maintenance](maintenance/index.md)

-   :fontawesome-solid-triangle-exclamation:{ .lg .middle } **Troubleshooting**

    ---

    Diagnose common hardware, Klipper and print-quality problems.

    [:octicons-arrow-right-24: Troubleshooting](troubleshooting/hardware-issues.md)

-   :material-download:{ .lg .middle } **Downloads**

    ---

    Access the current BOM, STL and CAD resources and see the status of firmware and slicer packages.

    [:octicons-arrow-right-24: Downloads](downloads/index.md)

</div>

## Rev A Technical Baseline

| Item | Rev A Definition |
|---|---|
| Build volume | 230 × 230 × 220 mm |
| Main voltage | 24 V DC |
| Controller | MKS Robin Nano V3 |
| Stepper drivers | 5 × TMC2209, UART |
| Host | Raspberry Pi Zero 2 W |
| Firmware | Klipper |
| Primary interface | Mainsail |
| Recommended slicer | OrcaSlicer |
| X/Y homing | TMC2209 sensorless homing |
| Z reference | P.I.N.D.A. probe |
| Local display | MKS TS35 V2.0 — integration under validation |

## Open-Source Documentation

The essential information required to build and understand the My-Cloner is maintained in this documentation and the associated project files.

Where a Rev A parameter has not yet been physically validated, the documentation keeps that limitation explicit instead of borrowing values from older prototypes or unrelated printers.

Start with the [Bill of Materials](bom/index.md), then continue through [Assembly](assembly/01_introduction.md), [Wiring & Electronics](wiring/index.md) and [Operation & Use](operation/index.md).
