# Connectivity Issues (USB, SD Card, Wi-Fi)

!!! abstract "The Problem"
    You can't get G-code files to your printer, or the connection drops mid-print. These problems relate to the communication link between your computer/host and the printer, whether it's a physical SD card, a USB cable, or a wireless network.

<figure markdown="1">
    ![Common connection methods for a 3D printer](/images/image-placeholder.png#only-light){ width="600" }
    ![Common connection methods for a 3D printer](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>An illustration of the common ways to connect to a 3D printer: via a USB cable, an SD card, or a Wi-Fi connection.</figcaption>
</figure>

## Common Problems and Solutions

### Problem: The printer is not reading the SD card.

* **Cause:** The card may be formatted incorrectly, is too large, has a corrupt file system, or is physically failing.
* **Solution:**
    1.  **Formatting:** This is the most common fix. SD cards must be formatted correctly. Use the official "SD Card Formatter" tool from the SD Association.
        * Cards ≤ 32GB should be formatted as **FAT32**.
        * Cards > 32GB should be formatted as **exFAT**, but be aware that many older printer firmwares do not support exFAT. Sticking to cards 32GB or smaller is safest.
    2.  **Keep it Simple:** Use simple filenames with no special characters. Don't use a card that is nearly full.
    3.  **Try Another Card:** SD cards wear out and fail. Try a different, preferably smaller (8GB or 16GB), card from a reputable brand (like SanDisk or Samsung). This is a very common point of failure.

### Problem: The computer doesn't recognize the printer over USB.

* **Cause:** Missing drivers for the printer's mainboard, a faulty USB cable, or a bad USB port.
* **Solution:**
    1.  **Check the Cable:** **Use a different USB cable.** Many cheap USB cables are for charging only and do not have the necessary data wires. Use a high-quality cable that you know supports data transfer, and keep it as short as possible.
    2.  **Install Drivers:** Your printer's mainboard uses a specific USB-to-serial chip to communicate (common types are CH340, FTDI, or WCH). You may need to manually find and install the driver for this chip on your computer. Check your printer manufacturer's documentation.
    3.  **Check Port/Computer:** Try a different USB port on your computer and restart the computer.

### Problem: Printing from a host (e.g., OctoPrint) randomly stops.

* **Cause:** This is often due to power issues with the host computer (like a Raspberry Pi) or communication errors from a poor-quality USB cable.
* **Solution:**
    1.  **Power Supply:** Ensure you are using the official, high-quality power supply for your Raspberry Pi or other single-board computer. A standard phone charger is often not powerful enough and will cause instability under load.
    2.  **USB Cable Quality:** This is critical. Use a short, high-quality USB cable, preferably one with ferrite beads to reduce electrical noise.
    3.  **The "5V Pin Tape" Trick (Advanced):** Some printer boards can try to draw power from the Raspberry Pi over USB, causing power issues. A common fix is to put a tiny piece of electrical tape over the 5V pin on the USB-A (the rectangular) end of the cable. This forces the printer to only use its own power supply.

### Problem: Wi-Fi connection is unstable or drops.

* **Cause:** Weak Wi-Fi signal or network interference.
* **Solution:**
    * Move the printer closer to your Wi-Fi router, or move the router closer to the printer.
    * Ensure the printer's Wi-Fi antenna (if it has an external one) is properly attached.
    * Check for sources of interference from other electronic devices, such as microwaves or cordless phones, near your printer or router.

## Quick Checklist
- [ ] If the SD card fails, try a different, smaller card (≤32GB).
- [ ] Format the SD card correctly using the official SD Card Formatter tool (FAT32).
- [ ] If USB fails, use a different, high-quality data cable.
- [ ] Install the correct USB-to-serial drivers for your printer board.
- [ ] Ensure your host computer (Raspberry Pi) has a sufficient, dedicated power supply.
