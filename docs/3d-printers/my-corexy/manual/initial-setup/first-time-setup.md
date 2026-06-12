# First Time Software Setup

This guide will walk you through installing the Klipper firmware on your Raspberry Pi and controller board (MCU).

### Step 1: Flash the Raspberry Pi SD Card

The easiest way to get started is by using an operating system image that comes pre-packaged with Klipper and a web interface.

1.  Download and install the **Raspberry Pi Imager** on your computer.
2.  Insert your microSD card into your computer.
3.  Run the imager and select an appropriate OS. **MainsailOS** or **FluiddPi** are excellent choices.
4.  Before writing the image, use the advanced options (cogwheel icon) to pre-configure your WiFi network details and enable SSH.
5.  Write the image to the SD card. Once complete, insert the card into your Raspberry Pi and power it on.

<figure markdown="1">
  ![Raspberry Pi Imager Interface](../../images/image-placeholder.png#only-light){ width="700" }
  ![Raspberry Pi Imager Interface](../../images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>The Raspberry Pi Imager software showing MainsailOS being selected as the operating system to be written to the SD card.</figcaption>
</figure>

### Step 2: Build the MCU Firmware

Now we need to build the firmware file that will be installed on your printer's main controller board.

1.  **Connect via SSH**: Find your printer's IP address and connect to it via SSH (e.g., `ssh pi@your_printer_ip`). The default password is often `raspberry`.
2.  Navigate to the Klipper directory: `cd ~/klipper`
3.  Run the configuration utility: `make menuconfig`
4.  In the menu, configure the settings to match your specific controller board (e.g., for a BTT Octopus, set the microcontroller architecture, processor model, and communication interface).
5.  Save and exit, then run `make` to build the firmware.

<figure markdown="1">
  ![Klipper make menuconfig Screen](../../images/image-placeholder.png#only-light){ width="800" }
  ![Klipper make menuconfig Screen](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>The Klipper `menuconfig` interface in the terminal, with options highlighted for a specific controller board like the BTT Octopus.</figcaption>
</figure>

### Step 3: Flash the MCU Firmware

1.  **Enter DFU Mode**: Follow your controller board's documentation to put it into DFU (bootloader) mode. This might involve a jumper or holding a button while powering it on.
2.  **Find Device ID**: From your SSH session, find the serial ID of your board with the command `ls /dev/serial/by-id/*`. Copy this ID.
3.  **Flash**: Run the command `make flash FLASH_DEVICE=your_copied_serial_id` to flash the firmware.

### Step 4: Configure Klipper

1.  In the web interface, navigate to the "Machine" or "Configuration" tab and open the `printer.cfg` file.
2.  You will need to use a sample configuration file as a base.
3.  Find the `[mcu]` section at the top of the file.
4.  Paste the serial ID you copied in the previous step as the value for the `serial:` parameter.
5.  Click "Save & Restart". If all goes well, Klipper will now be able to communicate with your printer's controller board.

<figure markdown="1">
  ![Editing the printer.cfg file](../../images/image-placeholder.png#only-light){ width="800" }
  ![Editing the printer.cfg file](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>The `printer.cfg` file open in the web interface editor, with the `[mcu]` section highlighted where the serial ID needs to be pasted.</figcaption>
</figure>