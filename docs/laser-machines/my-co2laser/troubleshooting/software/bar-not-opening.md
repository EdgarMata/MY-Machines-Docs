# Troubleshooting: Neon Studio Toolbar Not Appearing

The **Neon Studio Toolbar** is the essential control interface for operating your **Neon**. If this bar is missing, you will encounter errors such as *"No connection could be made because the target machine actively refused it"* when attempting to use "Neon It!" or "Preview."

Follow this guide to restore the control bar and resume your workflow.

---

## 1. Verifying Toolbar Status in Windows

The first step is to determine if the Toolbar process is running in the background but simply hidden from view.

1.  Right-click the **Windows Taskbar** and select **Task Manager**.
2.  Look for **"Neon Studio Toolbar"** in the list of active applications.

### If the Toolbar is listed:
It may be hidden or frozen. Right-click "Neon Studio Toolbar" and select **End Task**. You will then need to restart it manually (see Step 2).

### If the Toolbar is NOT listed:
The application failed to launch. Proceed to the manual activation steps below.

---

## 2. Manual Activation and Administrator Privileges

If the Toolbar does not launch automatically with **Neon Studio**, you can trigger it from the installation directory.

1.  Open Windows File Explorer and navigate to the following path:
    `C:\Program Files (x86)\Neon SA\Neon Studio\bin`
2.  Locate the file named **Neon Studio Toolbar.exe**.
3.  Double-click the file to launch the control bar manually.

### Pro Tip: Ensuring Permanent Launch
To prevent this issue from recurring, grant the application administrative rights:
1.  Right-click **Neon Studio Toolbar.exe** and select **Properties**.
2.  Under the **Compatibility** tab, check the box **"Run this program as an administrator"**.
3.  Click **OK**.
4.  Repeat these same steps for the **inkscape.exe** file located in the same folder.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Setting administrative privileges for the Neon control files (Coming Soon)</figcaption>
</figure>

---

## 3. Advanced Recovery (Reinstalling Core Files)

If the manual launch fails, some core files may be corrupted. You can restore the Toolbar by extracting a fresh copy of the binary folder.

1.  Download the **Neon Studio.rar** recovery package from the official support link.
2.  Locate the compressed file and right-click to **Extract Files**.
3.  Set the destination path directly to your **Local Disk (C:)**.
4.  Confirm the overwrite if prompted.

---

!!! success "System Restored"
    Once the files are replaced and the Toolbar is running as an administrator, the connection to your **Neon** should stabilize immediately.

---
**Still cannot see the Toolbar?**
If the control bar remains invisible after these steps, there may be a conflict with your antivirus or firewall settings. Contact **Neon Laser Support** for a remote technical session.