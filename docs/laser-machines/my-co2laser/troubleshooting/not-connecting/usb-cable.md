# Troubleshooting USB Connectivity

If your computer fails to establish a connection with the **Neon** via USB cable, the issue usually stems from driver conflicts, port management, or physical interface failure. This guide will walk you through a professional diagnostic sequence.

---

## 1. Verifying Hardware Recognition (OS Level)

The first step is to confirm if the Windows Operating System recognizes the **Neon's** internal interface.

1.  Open the **Device Manager** (Right-click the Start icon > Device Manager).
2.  Expand the **Ports (COM & LPT)** section.
3.  Look for an entry labeled **"USB-SERIAL CH340"**.

!!! tip "Diagnostic Trick"
    To confirm you have identified the correct port, unplug the USB cable from your computer and plug it back in. The "CH340" entry should disappear and reappear in the list.

---

## 2. Software and System Conflicts

### Bluetooth Signal Interference
Bluetooth adapters often create **Virtual COM Ports** that can conflict with the physical port assigned to the **Neon**. This "handshake" overlap prevents Due Studio from connecting.

**Solution:** Disable Bluetooth on your workstation during laser operation. 
* In Windows 11, use the Quick Settings panel (Taskbar corner) or go to **Settings > Bluetooth & Devices** and toggle the switch to **Off**.

### Application Hang-ups
Sometimes the Due Studio communication bridge becomes unresponsive.
* **Action:** Fully close Due Studio. Ensure the background process is terminated (check Task Manager if necessary) and relaunch the software to refresh the connection icon.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Video: Correctly restarting Due Studio communication (Coming Soon)</figcaption>
</figure>

---

## 3. Physical Interface and Cable Integrity

USB ports can suffer from "pin fatigue" or debris buildup, which allows peripheral devices (like mice) to work while failing to maintain the high-speed data stream required by the **Neon**.

### Sequential Testing:
1.  **Alternate Ports:** Connect the cable to a different USB port on your PC (avoid using unpowered USB hubs).
2.  **Cable Swap:** Test with a high-quality **USB 2.0 A-Male to B-Male** cable (commonly known as a printer cable).
3.  **Bypass the Extension:** The **Neon** uses an internal USB extension from the chassis (A) to the mainboard (B). To rule out a faulty extension:
    * Open the electronics bay using the Allen key.
    * Plug your USB cable **directly into the controller board port**.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Direct connection to the Neon controller board (Coming Soon)</figcaption>
</figure>

---

## 4. Alternative Diagnostic: Wi-Fi Test

If USB fails across all tests, attempt to connect via **Wi-Fi**. 
* **If Wi-Fi works:** The internal system and main controller are healthy, and the issue is strictly isolated to the USB serial chip or physical port.
* **If Wi-Fi also fails:** Check the controller's LED indicators. If the **Red Power LED** is off, the 12V power supply may not be reaching the board.

---

!!! info "Firmware Recovery"
    If the Device Manager recognizes the CH340 port but the software remains offline, the controller firmware may be corrupted. Contact **Due Laser Support** to obtain the latest firmware version and flashing instructions.

---
**Still Disconnected?**
Our technical team can perform a remote diagnostic to check your COM port assignments. Reach out to **Due Laser Support** for immediate assistance.