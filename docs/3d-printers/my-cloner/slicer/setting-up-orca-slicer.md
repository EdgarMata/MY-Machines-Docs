# Setting Up Orca Slicer

This guide will walk you through the initial setup of Orca Slicer, including importing the custom profile for your MY Cloner printer and connecting it to Klipper.

---
### Download and Install Orca Slicer

First, download the latest version of Orca Slicer for your operating system (Windows, macOS, or Linux) from their official GitHub page.

➡️ [**Download Orca Slicer Here**](https://github.com/SoftFever/OrcaSlicer/releases)

Install the software just as you would any other application.

### Initial Setup Wizard

When you open Orca Slicer for the first time, a setup wizard will appear.

1.  You can skip the initial printer selection, as we will be importing a custom profile.
2.  In the filament selection screen, it's a good idea to select **"Generic PLA"** and **"Generic PETG"** to start with.
3.  Complete the wizard.

### Importing the MY Cloner Printer Profile

This is the most important step to ensure all settings are optimized for your printer.

1.  In Orca Slicer, go to the top menu and click `File -> Import -> Import Configs...`.
2.  Navigate to and select the `MY_Cloner_Orca_Profile.ini` file that you downloaded.
3.  A window will pop up showing the profiles that will be imported. Ensure the printer profile is checked and click "Import."
4.  You should now see the "MY Cloner 3D Printer" available in the printer selection dropdown menu on the main screen.

### Connecting to Klipper via the "Device" Tab

This feature allows you to control your printer directly from Orca Slicer.

1.  Click on the **"Device"** tab in the left-hand sidebar.
2.  Click the "Add Printer" button.
3.  A dialog will appear. In the "Hostname" field, enter the IP address of your printer's Klipper host (e.g., `192.168.1.123`).
4.  Select "Klipper" from the firmware dropdown list.
5.  Click "OK."

You should now see your printer's web interface (Mainsail/Fluidd) appear directly within Orca Slicer. You can now upload files and start prints without leaving the application!

<figure markdown="1">
  ![Orca Slicer Device Tab](../../images/image-placeholder.png#only-light){ width="610" }
  ![Orca Slicer Device Tab](../../images/image-placeholder.png#only-dark){ width="610" }
  <figcaption>The network connection dialog in Orca Slicer's "Device" tab where you add your printer's IP address.</figcaption>
</figure>
