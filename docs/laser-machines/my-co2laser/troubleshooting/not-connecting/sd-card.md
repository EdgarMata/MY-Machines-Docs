# System Recovery: Flashing the SD Card

Operating anomalies or improper shutdowns can sometimes corrupt the system instructions stored on the **Neon's** internal SD card. If the controller's status LEDs indicate a communication failure, you will need to reflash the firmware image. 

---

## Pre-Diagnostic Checklist

Before proceeding with a system reflash, ensure you have ruled out secondary connectivity issues by reviewing these technical guides:

* **Hardware Status:** Analyzing Controller Board Activity (LED patterns).
* **Interface Issues:** Troubleshooting Ethernet and Wi-Fi Connections.

!!! info "Support Tip"
    The flashing process overwrites system data. If you have custom network configurations stored on the card, they may need to be reconfigured after the recovery.

---

## 1. Preparing the Imaging Software

To write the firmware image to the SD card, we recommend using **BalenaEtcher**, as it verifies the data integrity after flashing.

1.  **Download:** Obtain the BalenaEtcher installer from the official source.
2.  **Installation:** Run the executable and follow the setup wizard.
3.  **Initialization:** Open the application once the installation is complete.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Preparing the Flashing Environment (Coming Soon)</figcaption>
</figure>

---

## 2. Acquiring the Neon Firmware Image

1.  **Download the Image:** Download the latest **Neon Firmware Image** (.zip or .img).
2.  **Extraction:** Right-click the downloaded file and select "Extract" to a dedicated folder. Ensure you have the raw `.img` file ready for the flashing process.

---

## 3. Hardware Access and SD Removal

You will need the Allen key and the SD adapter provided in your **Neon Technical Kit**.

1.  **Power Down:** Completely disconnect the **Neon** from the power source.
2.  **Access the Controller:** Open the lateral electronics bay.
3.  **Eject the Card:** Locate the micro-SD slot on the mainboard and gently remove the card.
4.  **PC Connection:** Insert the micro-SD into the USB adapter and connect it to your computer.

---

## 4. The Flashing Procedure

!!! danger "Critical Warning: Drive Selection"
    Verify the target drive carefully. Flashing the wrong drive (like your PC's Hard Drive) will result in permanent data loss. The **Neon** SD card typically shows a capacity of 8GB or 16GB.

1.  **Select Image:** In BalenaEtcher, click **"Flash from file"** and select the extracted Neon `.img` file.
2.  **Select Target:** Choose the SD card reader as the destination drive.
3.  **Execute:** Click **"Flash!"** to begin the process.
4.  **Validation:** Wait for the software to finish the "Validating" stage to ensure the firmware was written without errors.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 2: Flashing Process in BalenaEtcher (Coming Soon)</figcaption>
</figure>

---

## 5. System Reinstallation

1.  **Reinsert the Card:** With the **Neon** still powered off, insert the SD card back into the mainboard slot. Ensure the gold contacts are facing the board.
2.  **Status Verification:** Power on the machine before closing the side panel. Check the **Yellow LED**; it should be pulsing, indicating active communication.
3.  **Connectivity Test:** Open Due Studio and attempt to establish a link.

---

!!! success "Recovery Complete"
    If the status LED is pulsing and the software connects, your **Neon** system is restored. You can now close the electronics bay and resume your projects.

---
**Still Offline?**
If the yellow LED remains solid or off after a successful flash, there may be a hardware fault with the SD card itself or the slot. Contact **Due Laser Support** for a replacement component.