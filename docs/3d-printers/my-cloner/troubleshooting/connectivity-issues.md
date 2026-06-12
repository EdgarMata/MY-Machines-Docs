# Connectivity Issues

With a Klipper-based printer, there are two main connection points that can cause issues: the connection from your computer to the printer's web interface (usually over Wi-Fi), and the USB connection between the host computer (e.g., Raspberry Pi) and the printer's mainboard (MCU).

---
### Web Interface Connection Issues (Wi-Fi / Ethernet)

**Symptom:** You cannot access the printer's web interface (Mainsail, Fluidd, etc.) from your browser. The page won't load or shows a "site can't be reached" error.

!!! info "This is a Network Problem"
    This means your computer cannot communicate with the Klipper host computer (e.g., Raspberry Pi). The printer itself might be on, but the host is offline or not on the network.

**Troubleshooting Steps:**

1.  **Check Host Power:** Is the Klipper host computer (Raspberry Pi) powered on? Check for its power and activity lights.
2.  **Verify Network Connection:**
    * **Wi-Fi:** Ensure the host is connected to the correct Wi-Fi network. A common issue after initial setup is a typo in the Wi-Fi password or network name.
    * **Ethernet:** Check that the Ethernet cable is securely plugged into both the host and your router/switch.
3.  **Find the Correct IP Address:** The IP address of the host may have changed. Log into your router's administration page and look for the list of connected devices to find the correct IP address for your printer's host (often named "mainsailos," "fluiddpi," or "raspberrypi").
4.  **Restart the Host:** A simple reboot of the Raspberry Pi can often solve temporary network glitches.

---
### Host to Printer MCU Connection Issues (USB)

**Symptom:** The web interface loads correctly, but it shows an error like `"MCU 'mcu' is not connected"` or `"Printer is not ready"`.

!!! info "This is a USB/Firmware Problem"
    This means the Klipper host (Raspberry Pi) cannot communicate with the printer's mainboard (MCU) over the USB cable.

**Troubleshooting Steps:**

1.  **Check the Physical USB Cable:** Ensure the USB cable between the host and the printer's mainboard is securely connected on both ends. Try a different, known-good data cable.
2.  **Verify the Serial Port in `printer.cfg`**
    * **Problem:** Klipper needs to know the exact "address" of your printer's mainboard on the USB bus. This can sometimes change after a reboot.
    * **Solution:**
        1.  Connect to your Klipper host via SSH (using a tool like PuTTY or the terminal).
        2.  Run the command: `ls /dev/serial/by-id/*`
        3.  This will output a long, unique name for your printer's board, like `/dev/serial/by-id/usb-Klipper_lpc1769_1E0002000740C8AFF5F66B5C-if00`.
        4.  Copy this entire path.
        5.  Open your `printer.cfg` file in the web interface and paste this path into the `serial:` line under the `[mcu]` section.
    * **Result:** Using the `by-id` path is more reliable and prevents the connection from breaking after a reboot.

    <figure markdown="1">
      ![Connectivity Issues](../images/image-placeholder.png#only-light){ width="600" }
      ![Connectivity Issues](../images/image-placeholder.png#only-dark){ width="600" }
      <figcaption>Illustration of various connection types (USB, SD card, Wi-Fi).</figcaption>
    </figure>

3.  **Check MCU Power:** Make sure the printer's mainboard has power. Some boards are powered by their own power supply, not just by the USB cable from the host.