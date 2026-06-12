# Thermal Safety

Your 3D printer uses high temperatures to melt plastic. This introduces two primary risks: severe burns from hot components and the potential for fire from uncontrolled heating.

### Burn Prevention
The hotend nozzle can reach temperatures over 250°C, and the heated bed can exceed 100°C.
* **Be Aware:** These components are hot enough to cause immediate and severe burns.
* **Cool-Down Time:** Remember that the hotend and bed remain dangerously hot for several minutes after the printer is turned off.
* **Silicone Sock:** Using a silicone sock on your heater block is highly recommended. It helps stabilize temperatures and provides a layer of protection against accidental contact.

<figure markdown="1">
  ![A hotend with a silicone sock installed](../../images/image-placeholder.png#only-light){ width="400" }
  ![A hotend with a silicone sock installed](../../images/image-placeholder.png#only-dark){ width="400" }
  <figcaption>A close-up of a hotend with a silicone sock fitted snugly around the heater block.</figcaption>
</figure>

### Thermal Runaway Protection
"Thermal runaway" is a dangerous condition where a failure (like a dislodged thermistor) causes the printer's firmware to lose track of the temperature. It may then try to heat the component indefinitely, creating a fire hazard.

* **Firmware Protection:** Klipper has a built-in safety feature to detect this. It will shut down the printer if the temperature does not rise as expected when a heater is on, or if the temperature is dangerously out of range. You must ensure this feature is enabled and correctly configured in your `printer.cfg`.
* **Hardware Protection (Thermal Fuse):** Your heated bed is equipped with a physical thermal fuse. This is a one-time-use safety device that physically cuts power to the bed if it ever exceeds a critical temperature (e.g., 120°C). It is a last line of defense and should never be bypassed.