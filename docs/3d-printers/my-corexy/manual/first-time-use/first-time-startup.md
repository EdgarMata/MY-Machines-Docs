# First Time Startup

This is an exciting and critical moment. The goal of this first power-on is to perform a "smoke test"—a brief, careful check to ensure the electronics power up safely without any short circuits or major issues. The key is to be cautious and ready to cut power instantly if anything seems wrong.

### Step 1: Final Safety Check

Before plugging anything in, perform one last visual inspection of the electronics bay.

* Check for any loose wires or stray wire strands that could cause a short.
* Ensure no tools (screws, hex keys, etc.) have been left on or near the electronics boards.
* Confirm that all screw terminals are tight.

!!! danger "Fire Extinguisher Ready"
    For this first power-on, it is highly recommended to have an appropriate fire extinguisher within arm's reach, just in case.

### Step 2: 5V Power-On (Raspberry Pi)

1.  Plug your printer's main power cord into the wall outlet, but leave the main power switch on the printer **OFF**.
2.  Your 5V power supply should now provide power to your Raspberry Pi. You should see indicator lights on the Pi turn on.
3.  On your computer, navigate to the web interface (Mainsail, Fluidd, etc.). The interface should load, but it will likely show an error stating that it cannot connect to the MCU. This is normal and expected, as the main controller board is still off.

<figure markdown="1">
  ![Web interface showing MCU connection error](../../images/image-placeholder.png#only-light){ width="800" }
  ![Web interface showing MCU connection error](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>The web interface showing a "Klippy host is not connected" or similar error message before the main 24V power is turned on.</figcaption>
</figure>

### Step 3: The "Smoke Test" (24V Power-On)

!!! warning "Be Ready to Power Off Immediately"
    Keep your hand on the main power switch for this entire step. Be prepared to turn it off instantly if you see, hear, or smell anything unusual.

1.  Take a deep breath and flip the main power switch **ON**.
2.  **Look, listen, and smell.** You are watching for any sparks, smoke, or a distinct "magic smoke" smell of burning electronics. You are listening for any loud pops or cracks.
3.  If any of these things occur, **TURN THE POWER OFF IMMEDIATELY** and return to the wiring section to troubleshoot.
4.  If all is well, the fan on your 24V PSU may spin up for a moment, and you should see lights turn on on your main controller board.

### Step 4: Establish MCU Connection

If the smoke test was successful, your printer is now fully powered.

1.  In the web interface, click the "FIRMWARE RESTART" or "RESTART" button.
2.  After a few moments, the error message should disappear. The interface will now show live temperature readings from your hotend and heated bed thermistors.

<figure markdown="1">
  ![Web interface successfully connected to the MCU](../../images/image-placeholder.png#only-light){ width="800" }
  ![Web interface successfully connected to the MCU](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>The web interface now successfully connected, displaying ambient temperature readings for the hotend and bed.</figcaption>
</figure>

Congratulations! You have successfully and safely powered on your printer for the first time. In the next chapter, we will perform pre-flight checks before attempting any movement.
