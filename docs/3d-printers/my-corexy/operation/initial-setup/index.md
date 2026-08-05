# Initial Setup: Introduction

Congratulations on completing the physical assembly of your printer! The hard part is over. This section of the manual will guide you through the next critical phase: installing and configuring the software that runs your machine.

This printer runs on **Klipper**, a powerful firmware that uses a Raspberry Pi for heavy processing, resulting in higher print speeds and quality. The setup process involves:

1.  **Installing the Klipper software** on your Raspberry Pi.
2.  **Flashing the Klipper firmware** to your main controller board (MCU).
3.  **Configuring the printer** to match your specific hardware.
4.  **Learning the web interface** to control your new machine.

Once this section is complete, you will have a fully operational printer, ready for calibration and printing.

<figure markdown="1">
  ![Klipper Software Architecture Diagram](/assets/images/image-placeholder.webp#only-light){ width="800" }
  ![Klipper Software Architecture Diagram](/assets/images/image-placeholder.webp#only-dark){ width="800" }
  <figcaption>A diagram showing the Klipper software architecture: The user's computer communicates via a web browser to the Web Interface (Mainsail/Fluidd), which runs on the Raspberry Pi alongside the Klipper host software. The Pi then sends commands to the printer's main controller board (MCU).</figcaption>
</figure>
