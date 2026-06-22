# Belt Tensioning Guide

On a CoreXY printer, correct and consistent belt tension is one of the most critical factors for achieving high print quality.
* **Loose belts** will cause "ghosting" or "ringing" artifacts and can lead to poor dimensional accuracy.
* **Overly tight belts** will put excessive stress on the motor bearings and idlers, leading to premature wear and potential motion issues.

### The Quantitative Method (Recommended)

The most accurate and repeatable way to set belt tension is by measuring the frequency of the belt's vibration, much like tuning a guitar string. You will need a smartphone with a spectrum analyzer app (such as "Sound Analyser" on Android or "Decibel X" on iOS).

#### A/B (CoreXY) Belts

1.  **Position Toolhead**: Move the toolhead to the center of the X-axis. Move the gantry so the toolhead is approximately 150mm away from the rear idlers.
2.  **Measure Frequency**: Hold your phone's microphone close to the longest, top span of the **A-belt**. Gently "pluck" the belt with your finger. The analyzer app should show a peak frequency.
3.  **Adjust Tension**: Adjust the A-belt's tensioner until the peak frequency is approximately **110 Hz**.
4.  **Repeat**: Repeat the exact same process for the **B-belt**. It is crucial that both belts are tensioned to the same frequency.

<figure markdown="1">
  ![Using a phone app to measure belt tension frequency](/images/image-placeholder.png#only-light){ width="700" }
  ![Using a phone app to measure belt tension frequency](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>A smartphone with a frequency analyzer app held close to a 3D printer belt that is being plucked by a finger. The app displays a clear frequency peak.</figcaption>
</figure>

#### Z-Axis Belts

1.  **Position Gantry**: Move the gantry to roughly the middle of its Z-axis travel.
2.  **Measure Frequency**: Pluck one of the vertical Z-belts and measure its frequency.
3.  **Adjust Tension**: Adjust the Z-belt's tensioner until the frequency is approximately **140 Hz**.
4.  **Repeat**: Repeat for the other three Z-belts, ensuring they are all tensioned as equally as possible.

### The Qualitative Method (Quick Check)

For quick weekly checks, you don't need to use the frequency method every time. Simply pluck the belts and get a feel for their tension. They should be taut and produce a low, audible tone. The key is to ensure they feel consistent with each other and haven't become noticeably loose over time.