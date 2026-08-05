# Calibrating Input Shaper 

Input Shaping is one of Klipper's most powerful features. It is designed to cancel out the vibrations (resonant frequencies) of your printer's frame, which eliminates the "ringing" or "ghosting" artifacts that appear after corners and sharp details in your prints. Correctly calibrating Input Shaper is the key to printing at high speeds without sacrificing quality.

### Required Hardware: ADXL345 Accelerometer

To use the automated calibration process, you will need a small, inexpensive sensor called an **ADXL345 accelerometer**. This sensor is temporarily mounted to the toolhead to physically measure the frame's vibrations during a test sequence.

<figure markdown="1">
  ![An ADXL345 accelerometer ready for installation](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![An ADXL345 accelerometer ready for installation](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>An ADXL345 accelerometer with its connecting wires, ready to be mounted on the toolhead.</figcaption>
</figure>

### The Calibration Process

1.  **Mount the Sensor**: Securely mount the ADXL345 accelerometer to your toolhead. It must be mounted rigidly; any wobble in the sensor will produce poor results.
2.  **Configure Klipper**: Add the `[adxl345]` and `[resonance_tester]` sections to your `printer.cfg` file. You will need to refer to the official Klipper documentation for the correct pin configuration depending on how you wired the sensor (via SPI or I2C).
3.  **Run the Test**: Heat your bed to its typical operating temperature and let the machine sit for a few minutes so the frame temperature stabilizes. In the console, run the command: `SHAPER_CALIBRATE`
4.  The printer will now perform a series of rapid, vibrating movements on both the X and Y axes to measure the resonant frequencies.
5.  **Save the Results**: Once the test is complete, Klipper will output its recommendations in the console, suggesting the best shaper type (e.g., `mzv` or `ei`) and the measured frequency for each axis.
6.  Type `SAVE_CONFIG` in the console. Klipper will automatically write the recommended `[input_shaper]` configuration to your `printer.cfg` file.
7.  Once saved, you can remove the sensor and delete or comment out the `[adxl345]` and `[resonance_tester]` sections from your config.

### The Result

The difference in print quality before and after calibration is dramatic.

<figure markdown="1">
  ![A before-and-after ringing test print](/assets/images/image-placeholder.webp#only-light){ width="700" }
  ![A before-and-after ringing test print](/assets/images/image-placeholder.webp#only-dark){ width="700" }
  <figcaption>A side-by-side comparison of two ringing test towers. The "before" print shows significant ghosting artifacts after the corners, while the "after" print with Input Shaper is perfectly clean and sharp.</figcaption>
</figure>
