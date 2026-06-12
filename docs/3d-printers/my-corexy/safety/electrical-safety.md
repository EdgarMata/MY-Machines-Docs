# Electrical Safety

!!! danger "Lethal Voltage Hazard"
    Mistakes when working with mains electricity (110V/230V) can be fatal. This is the most significant danger associated with building a DIY printer. If you are not completely comfortable and knowledgeable about high-voltage wiring, **stop and consult a qualified electrician.**

### Always Unplug the Printer
Before you open the electronics bay or perform any maintenance, physically disconnect the power cord from the wall outlet. Simply turning off the power switch is not enough.

### Proper Grounding (Protective Earth)
Grounding is a critical, non-negotiable safety feature. It provides a safe path for electricity to flow in the event of a short circuit, tripping your circuit breaker instead of electrocuting you.
* The **Protective Earth (PE)** wire from your mains inlet must be securely connected to the metal frame of the printer, the metal casing of your power supply unit(s), and the ground screw on your heated bed.

<figure markdown="1">
  ![Diagram showing proper grounding path](../../images/image-placeholder.png#only-light){ width="800" }
  ![Diagram showing proper grounding path](../../images/image-placeholder.png#only-dark){ width="800" }
  <figcaption>A wiring diagram highlighting the path of the Protective Earth (ground) wire from the mains inlet to the printer's frame, PSU casing, and heated bed.</figcaption>
</figure>

### Secure Connections
Loose high-voltage connections can create arcs and are a major fire hazard.
* **Use Ferrules:** For connecting stranded wire to screw terminals (like on a PSU), always use crimped wire ferrules. Tinning the wire ends with solder is not a safe alternative, as the solder can deform ("creep") over time, causing the connection to become loose.

<figure markdown="1">
  ![Comparison of a tinned wire vs a crimped ferrule](../../images/image-placeholder.png#only-light){ width="600" }
  ![Comparison of a tinned wire vs a crimped ferrule](../../images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>A side-by-side comparison showing a poorly-tinned wire end next to a stranded wire that has been properly terminated with a crimped ferrule, ready for a screw terminal.</figcaption>
</figure>

### Power Supply Units (PSUs)
Never open the metal casing of a power supply unit. They contain large capacitors that can hold a dangerous charge long after being unplugged. Ensure your PSU has adequate ventilation and is not covered.