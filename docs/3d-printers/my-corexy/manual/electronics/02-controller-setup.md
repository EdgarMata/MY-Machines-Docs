# Step 10: Controller Board Setup

Before connecting any wires, you must configure the main controller board by setting jumpers correctly. These jumpers control critical functions like the communication mode for the stepper drivers and the voltage supplied to the fans.

!!! danger "Incorrect Jumper Settings Can Damage Your Board"
    Double-check every jumper placement against the documentation for your specific controller board. Applying the wrong voltage to a component can destroy it instantly.

### Step 1: Jumper Configuration

1.  **Start Clean**: It's often easiest to remove all jumpers from the board to start from a known state.
2.  **Set Driver Mode**: For TMC2209 drivers, place jumpers to enable UART mode. This allows for advanced control via the firmware.
3.  **Set Fan Voltages**: Place jumpers to select the correct voltage for your fans (typically 24V). Your hotend fan, part cooling fan, and electronics fans must all match the voltage you select here.
4.  **Set Probe Voltage**: Set the jumper for the probe input voltage to match your inductive probe's requirements (typically 24V).

<figure markdown="1">
  ![Controller board jumper configuration](../../../../images/image-placeholder.png#only-light){ width="800" }
  ![Controller board jumper configuration](../../../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>A diagram showing the controller board with jumpers correctly placed for UART mode, 24V fan voltage, and 24V probe voltage.</figcaption>
</figure>

### Step 2: Stepper Driver Installation

Carefully install the stepper motor drivers (e.g., TMC2209) into their sockets.

!!! warning "Check Orientation"
    Stepper drivers can only be inserted one way. Align the pins correctly before applying pressure. Installing a driver backwards will destroy it and potentially the controller board when powered on.

<figure markdown="1">
  ![Installing the stepper drivers](../../../../images/image-placeholder.png#only-light){ width="600" }
  ![Installing the stepper drivers](../../../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>TMC2209 stepper drivers being carefully installed into the sockets on the controller board, with pin orientation clearly visible.</figcaption>
</figure>

### Step 3: Pinout Reference

Keep the pinout diagram for your board handy. You will need it for every connection in the upcoming wiring chapters.

<figure markdown="1">
  ![Controller board pinout diagram](../../../../images/image-placeholder.png#only-light){ width="900" }
  ![Controller board pinout diagram](../../../../images/image-placeholder.png#only-dark){ width="900" }
  <figcaption>A detailed pinout diagram of the controller board for reference during the wiring process.</figcaption>
</figure>