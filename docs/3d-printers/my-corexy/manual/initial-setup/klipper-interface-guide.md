# Klipper Interface Guide

The web interface (Mainsail or Fluidd) is your command center. It allows you to control every aspect of your printer from a web browser on any device on your network.

<figure markdown="1">
  ![Annotated Web Interface Dashboard](/images/image-placeholder.png#only-light){ width="900" }
  ![Annotated Web Interface Dashboard](/images/image-placeholder.png#only-dark){ width="900" }
  <figcaption>The main dashboard of the web interface, with key areas highlighted: Temperature Graphs, Console, G-Code Viewer, Job Status, and Movement Control Buttons.</figcaption>
</figure>

### Key Interface Sections

* **Dashboard**: This is your main overview screen. You can monitor temperatures, see the webcam feed, check print job progress, and access emergency stop functions.
* **Console**: This is a direct command line to your printer. You can send G-code commands manually (e.g., `G28` to home) and see real-time responses and logs from Klipper.
* **Temperature Control**: This area displays live temperature graphs and allows you to manually set target temperatures for your hotend and heated bed.
* **Movement Controls**: Here you can find buttons to home the X, Y, and Z axes, disable motors, and manually move (jog) the toolhead along each axis.
* **File Management**: This section lists all your uploaded G-code files. You can upload new files, delete old ones, and start prints from here.
* **Configuration**: This powerful feature gives you a built-in text editor to view and modify your `printer.cfg` and any other Klipper configuration files directly from your browser.