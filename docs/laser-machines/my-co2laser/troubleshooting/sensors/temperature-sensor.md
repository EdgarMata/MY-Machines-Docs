# Thermal Safety: Water Temperature Monitoring

The **Neon** includes a real-time thermal protection system. To ensure the longevity of the CO2 laser tube, the machine monitors the coolant temperature and will pause operations if it exceeds safe operational limits.

---

## Temperature Thresholds

The software provides feedback based on the following thermal states:

* **Warning State (35°C / 95°F):** The system will notify you that the water is getting warm. You can continue working, but it is recommended to monitor the cooling efficiency.
* **Safety Pause (40°C / 104°F):** For the protection of the laser tube, the **Neon** will automatically pause the current job. 

!!! info "Auto-Resume Feature"
    When a Safety Pause occurs, the machine will wait until the temperature drops below **35°C** before automatically resuming the work exactly where it left off. You do not need to intervene.

---

## How to Check Current Temperature

You can monitor the thermal status directly in the **Due Studio** control panel.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Locating the temperature readout in Due Studio (Coming Soon)</figcaption>
</figure>

---

## Best Practices for Cooling

If your working environment is naturally hot and you do not have air conditioning, consider these tips:

1.  **Chilled Water:** You may replace the reservoir water with fresh, chilled water (around 15°C / 59°F). *Note: Do not use ice or frozen water, as extreme temperature shocks can crack the glass tube.*
2.  **Ventilation:** Ensure the **Neon's** radiator intake is not obstructed and has access to cool air flow.
3.  **Duty Cycle:** On extremely hot days, allow the machine brief resting periods between long cutting jobs.

---
**Persistent Overheating?**
If your machine reaches 40°C too quickly, there may be an issue with the radiator or ambient airflow. Contact **Due Laser Support** for a cooling system evaluation.