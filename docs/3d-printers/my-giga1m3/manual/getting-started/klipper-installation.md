# Klipper Installation

<figure markdown="span">
  ![](../../images/Under_Construction.svg#only-light){ width="610" }
  <figcaption></figcaption>
  ![](../../images/Under_Construction.svg#only-dark){ width="610" }
  <figcaption></figcaption>
</figure>

Welcome to the complete guide for installing and configuring Klipper.

This manual was created to help you set up a dedicated Klipper machine from scratch, using the command line. Each part of the guide is designed to be as clear and simple as possible, with practical examples and all necessary commands.

---

<figure markdown="span">
  ![](images/Under_Construction.svg#only-light){ width="610" }
  <figcaption></figcaption>
  ![](images/Under_Construction.svg#only-dark){ width="610" }
  <figcaption></figcaption>
</figure>

---

### **Prerequisites**

Before you start, make sure you have the following:

  * The Debian **Netinstall image with non-free firmware**.
  * A USB stick with at least 4GB capacity.
  * The machine where you will install Debian and its USB Wi-Fi adapter.

---

### **Part 1: Install Debian (OS)**

1.  **Prepare the USB Stick**:
    * Use a program like **BalenaEtcher** or **Rufus** to write the Debian image to the USB stick.

2.  **Start the Installation**:
    * Plug the USB stick into the computer and boot from it (you may need to change the boot order in BIOS/UEFI).

3.  **Set User and Password**:
    * Follow the installer instructions. When prompted to set the **`root`** password, use **`machines`**.
    * When creating a user, set the username as **`mymachines`** and the password as **`machines`**.
    * (Note: During installation, when asked about the network, choose "Do not configure the network now." We'll do this later to avoid conflicts.)

4.  **Software Selection**:
    * When you reach the **"Software selection"** screen, it is crucial to **deselect** all desktop environment options (like GNOME, KDE Plasma, etc.).
    * For a command-line-only installation, make sure **only the following options are selected**:
        * **SSH server**
        * **Standard system utilities**

---

### **Part 2: Configure Superuser Access**

After installation, your user (`mymachines`) does not have permissions to run administrator commands. Let's fix that.

1.  **Log in as `root`**:
    * Open the Terminal.
    * Switch to the `root` user with the following command and use the password you set for `root` (**`machines`**).
      ```bash
      su -
      ```

2.  **Install `sudo`**:
    * Now that you have administrator permissions, install the **`sudo`** package.
      ```bash
      apt update
      apt install sudo -y
      ```

3.  **Add User to `sudo` Group**:
    * Add your user **`mymachines`** to the administrators group.
      ```bash
      usermod -aG sudo mymachines
      ```

4.  **Exit `root` and Reboot**:
    * For the changes to take effect, exit the `root` session and reboot the machine.
      ```bash
      exit
      reboot
      ```

---

### **Part 3: Configure Wi-Fi Connection**

After the machine has rebooted, log in with your user (**`mymachines`**). **Do not plug in the network cable!**

1.  **Find the Wi-Fi Interface Name**:
    * Open the Terminal and run the following command:
      ```bash
      ip a
      ```
    * Look for an interface that starts with **`wl`**. The name of your interface is **`wlxc4e984ddf898`**.

2.  **Install Essential Packages**:
    * For Wi-Fi to work, we need **`wpa_supplicant`** and the DHCP client.
      ```bash
      sudo apt update
      sudo apt install wpasupplicant isc-dhcp-client -y
      ```
    * You also need to create the `wpa_supplicant` configuration directory.
      ```bash
      sudo mkdir /etc/wpa_supplicant
      ```

3.  **Generate the Wi-Fi Configuration File**:
    * This command generates a secure configuration file with your encrypted password. Replace `"YourSSID"` and `"YourPASSWORD"` with your details.
      ```bash
      sudo wpa_passphrase "YourSSID" "YourPASSWORD" | sudo tee /etc/wpa_supplicant/wpa_supplicant-wlxc4e984ddf898.conf
      ```

4.  **Configure `interfaces` for Automatic Connection**:
    * Open the network configuration file.
      ```bash
      sudo nano /etc/network/interfaces
      ```
    * At the end of the file, add these lines to ensure the connection is established automatically at boot.
      ```
      # The wireless network interface
      allow-hotplug wlxc4e984ddf898
      iface wlxc4e984ddf898 inet dhcp
          wpa-roam /etc/wpa_supplicant/wpa_supplicant-wlxc4e984ddf898.conf
      ```
    * Save (`Ctrl + O`, `Enter`) and exit (`Ctrl + X`).

5.  **Restart the Networking Service**:
    * For the changes to take effect.
      ```bash
      sudo systemctl restart networking
      ```

6.  **Check the Connection**:
    * Use the `ip a` command again. Your interface **`wlxc4e984ddf898`** should have an IP address.

---

### **Part 4: Access the Machine Remotely (SSH)**

Since you selected the option to install the SSH server during OS installation, you don't need to install it manually. Just connect.

1.  **Access the Machine Remotely**:
    * From another computer, use the Terminal, PowerShell, or `cmd` to connect. Replace the IP address with the one your Debian machine obtained in the previous step.
      ```bash
      ssh mymachines@your_machine_IP_address
      ```
    * Enter the password for user **`mymachines`** (**`machines`**) when prompted.
    * (Note: If the connection fails, the SSH server may not have been installed correctly. In that case, you can install it manually with `sudo apt install openssh-server -y`.)

---

### **Part 5: Install Klipper and Its Components**

1.  **Install `git`**:
    * `git` is essential. If it is not installed, use `sudo` to install it.
      ```bash
      sudo apt install git -y
      ```

2.  **Run the Automatic Installer**:
    * Navigate to your home folder and download the **`kiauh`** script.
      ```bash
      cd ~
      git clone https://github.com/th33xitus/kiauh.git
      cd kiauh
      ./kiauh.sh
      ```

3.  **Install the Components**:
    * In the **`kiauh`** menu, select `1` (Install) and choose the components in the following order:
        * **Klipper**
        * **Moonraker**
        * **Mainsail** (or Fluidd, as you prefer)

4.  **Install the Firmware on the Printer Board**:
    * Go back to the main menu and select `4` (Build/Flash Firmware). `kiauh` will guide the process. This step is crucial and varies depending on your controller board.

---

### **Part 6: Configure and Access Klipper**

1.  **Access the Web Interface**:
    * Open your favorite web browser and, in the address bar, type the IP address of your Debian machine.
    * The **Mainsail** interface should load.

2.  **Final Configuration**:
    * In the Mainsail interface, the last step is to upload your configuration file (`printer.cfg`) in the "Configuration" section.

---

### **Part 7: Install Firmware on MCUs and Configure in Mainsail**

1.  **Install Firmware on MCUs**
    * For Klipper to communicate with your boards, you need to flash the firmware. Even if you have already done this, it is a crucial step in the process.
    * Make sure your MCUs are connected to the Debian computer via USB.
    * Open the terminal, navigate to the `kiauh` folder, and start the script:
      ```bash
      cd ~/kiauh
      ./kiauh.sh
      ```
    * In the `kiauh` menu, select option **`4` (Build/Flash Firmware)** and follow the on-screen instructions to compile and install the firmware on each of your boards (the main and the heated bed).

2.  **Find the MCU Address**
    * After the firmware is installed, you need to find the correct USB ports. Run the following command in the Terminal to list the devices.
      ```bash
      ls /dev/serial/by-id/*
      ```
    * The command should return the path for your MCUs. You will see a path for each board. Example:
        * `/dev/serial/by-id/usb-Klipper_lpc1768_123456789ABC-if00` (for the main MCU)
        * `/dev/serial/by-id/usb-Klipper_lpc1768_987654321DEF-if00` (for the heated bed MCU)

3.  **Add the Addresses to the `printer.cfg` File (in Mainsail)**
    * In the Mainsail web interface, click the **"Configuration"** icon (usually a screwdriver).
    * In the left menu, select the **`printer.cfg`** file.
    * Edit the MCUs section in the file, inserting the following lines. **Replace the example addresses** with those you found in the previous step.
      ```
      [mcu]
      serial: /dev/serial/by-id/usb-Klipper_lpc1768_123456789ABC-if00

      [mcu heatbed]
      serial: /dev/serial/by-id/usb-Klipper_lpc1768_987654321DEF-if00
      ```
4.  **Configure Pins (Example)**
    * From here, you can continue configuring your printer's components. For example, when configuring the heated bed, refer to the second MCU.
      ```
      [heater_bed]
      heater_pin: heatbed:PA2
      ...etc...
      ```

---

### **Part 8: Configure Hostname for Local Access**

1.  **Change the Machine Name**
    * Open the `/etc/hostname` file with `nano` and `sudo`:
      ```bash
      sudo nano /etc/hostname
      ```
    * Delete what is there and write only the new name:
      ```
      my-giga1m3
      ```
    * Save (`Ctrl + O`, `Enter`) and exit (`Ctrl + X`).

2.  **Edit the `hosts` File**
    * Open the `/etc/hosts` file with `nano` and `sudo`:
      ```bash
      sudo nano /etc/hosts
      ```
    * Look for the line that starts with `127.0.1.1` and make sure the name `my-giga1m3` is at the end of the line, or add the following line if it does not exist.
      ```
      127.0.1.1  my-giga1m3
      ```
    * Save (`Ctrl + O`, `Enter`) and exit (`Ctrl + X`).

3.  **Install the `Avahi` Service (mDNS)**
    * This is the crucial step for the `.local` name to work. `Avahi` is the service that enables name resolution on your local network.
      ```bash
      sudo apt install avahi-daemon -y
      ```
    * The service will be activated automatically after installation.

4.  **Reboot Your Machine**
    * For all changes to take effect, you need to reboot the system.
      ```bash
      sudo reboot
      ```

      
<figure markdown="span">
  ![](images/Under_Construction.svg#only-light){ width="610" }
  <figcaption></figcaption>
  ![](images/Under_Construction.svg#only-dark){ width="610" }
  <figcaption></figcaption>
</figure>