# Understanding Start From Modes in LightBurn

LightBurn offers three primary methods to define how a job runs in relation to your workspace coordinates and the laser head's location: **Absolute Coordinates**, **Current Position**, and **User Origin**.

## Preliminary: Enabling the Fire Button
Before using these modes, it is helpful to enable the laser fire button for alignment:
* Go to **Device Settings** (wrench icon).
* Enable **"Enable laser fire button"**.
* In the **Move window**, set the power to a low value (1-2%) to see the beam without marking the material.

---

## 1. Absolute Coordinates
This is the most straightforward mode, ideal for beginners or machines with limit switches.
* **How it works**: The grid on your screen represents the physical work area of your machine.
* **Placement**: If you place a design in the center of the LightBurn workspace, it will engrave exactly in the center of your laser's bed.
* **Setup**:
    * **With Limit Switches**: The machine homes automatically. Simply select "Absolute Coordinates" and run the job.
    * **Without Limit Switches**: Manually move the laser head to the origin (usually front-left) before powering on the machine. This point becomes (0,0).

## 2. Current Position
This mode is best for quick jobs or irregularly shaped items like coasters.
* **How it works**: The job starts relative to wherever the laser head is currently positioned.
* **Job Origin Grid**: You must tell LightBurn which part of the design corresponds to the laser's current spot (e.g., if the laser is over the center of your material, select the center dot in the "Job Origin" grid).
* **Pro Tip**: Make a small pencil mark in the center of your object to align the laser beam accurately before starting.

## 3. User Origin
Similar to Current Position, but allows you to save a specific starting point.
* **How it works**: You define a "Home" spot for that specific job.
* **Setup**:
    * Use the **Move window** to jog the laser to your desired starting point.
    * Click **Set Origin**.
    * Ensure the **Job Origin grid** matches the location you just set (e.g., if you set the origin at the top-left of your work, select top-left in the grid).
* **Benefit**: You can move the laser head away to check the work and easily return to the exact starting point by clicking "Go to Origin".

---
*Source: LightBurn Software Official Tutorials*