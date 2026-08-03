# Banding (Horizontal Lines)

"Banding" (or "Z-Banding") is a print quality defect that manifests as regular horizontal lines or repeating patterns on the vertical walls of a print.

!!! info "What Causes Banding?"
    This problem is generally caused by mechanical inconsistencies in the Z-axis or by fluctuations in extrusion.

---
### Causes and Solutions

1.  **Mechanical Z-Axis Issues**
    * **Cause:** The Z-axis rods or lead screws may be dirty, bent, or poorly lubricated. This causes friction and prevents the Z-axis from consistently moving up by the same small amount for each layer, resulting in some layers being more "squished" than others.
    * **Solution:** Clean and lubricate the Z-axis rods/screws. Check if they are bent by rolling them on a flat surface. Also, ensure the couplers connecting the motors to the lead screws are tight.

2.  **Hotend Temperature Fluctuations**
    * **Cause:** If the nozzle temperature is not stable and varies by several degrees, the consistency of the extruded plastic will also vary. Hotter plastic flows more easily, creating a slightly wider line, and vice-versa.
    * **Solution:** Perform a **PID Tune** of the hotend. This function, available in most printer menus, adjusts the heating algorithm to keep the temperature as stable as possible.

3.  **Filament Inconsistency**
    * **Cause:** Low-quality filaments can have variations in their diameter along the spool. A thicker section results in more extrusion (a more prominent line), and a thinner section results in less.
    * **Solution:** Use high-quality filament with a good reputation for diameter consistency.

<figure markdown="1">
  ![Z-Banding Example](/assets/images/image-placeholder.webp#only-light){ width="600" }
  ![Z-Banding Example](/assets/images/image-placeholder.webp#only-dark){ width="600" }
  <figcaption>Illustration of a part with vertical walls that show a pattern of repeating horizontal lines.</figcaption>
</figure>
