# Hardware Diagnostics: Controller Board Activity

If you are experiencing persistent connectivity issues that were not resolved by basic network or cable troubleshooting, the next step is to analyze the physical state of the **Neon's** internal controller. This guide focuses on diagnosing the mainboard through its integrated LED indicators.

---

## Preliminary Troubleshooting

Before inspecting the internal electronics, ensure you have already ruled out external factors by consulting these guides:

* **Network Stability:** Troubleshooting Ethernet Connections.
* **Access Point Issues:** Troubleshooting the **Neon** Wi-Fi Network.
* **Network Integration:** Troubleshooting Local Workplace Wi-Fi.

If the communication fault persists, follow the diagnostic steps below.

---

## 1. Accessing the Electronics Bay

To inspect the controller, you must access the machine's lateral compartment. 

!!! danger "Safety Requirement"
    Ensure the machine is powered down before opening any protective panels. Use the Allen key provided in your technical support kit to remove the side cover.

<figure markdown="span">
  ![](../images/construcao-light.png#only-light){ width="400" }
  ![](../images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Video: Opening the Neon Electronics Compartment (Coming Soon)</figcaption>
</figure>

---

## 2. Analyzing Controller LED Indicators

The **Neon** mainboard features two primary LEDs that provide real-time feedback on power status and data synchronization with the SD card.

### Power Status (Red LED)
The solid **Red LED** indicates that the board is receiving the correct voltage. 
* **If the LED is OFF:** The board is not powered. Check the physical seating of the internal pins that bridge the upper and lower boards. Ensure all connections are firm and debris-free.

### SD Card Communication (Yellow LED)
Next to the power indicator, you should observe a **flashing Yellow LED**. This pulsing signal confirms active data exchange between the controller and the SD card.
* **If the LED is OFF or Solid:** The communication has failed, likely due to a corrupted SD card. In this case, the card must be reflashed. Please refer to our guide on **SD Card Recovery and Reflashing**.

<figure markdown="span">
  ![](../images/construcao-light.png#only-light){ width="400" }
  ![](../images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Video: Identifying Board Status LEDs (Coming Soon)</figcaption>
</figure>

---

!!! info "Technical Recovery"
    If the LEDs indicate proper power and communication but the **Neon** remains offline, the issue may reside in the firmware or deep network configurations.

---
**Need Specialist Support?**
Hardware diagnostics can be complex. If you are unsure about the LED patterns or the state of your controller, contact **Due Laser Support** to perform a guided inspection with our technicians.