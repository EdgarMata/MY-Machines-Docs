# Vectorizing Images in Neon Studio (Trace Bitmap)

Vectorizing is the process of converting a pixel-based image (like a JPEG or PNG) into paths (vectors) that the **Neon** can follow for cutting or high-definition engraving. This guide shows you the fastest way to "trace" your images.

---

## 1. Import your Image
Go to **File > Import...** (or press `Ctrl + I`) and select the image you want to vectorize.

## 2. Opening the Trace Tool
Once your image is selected in the workspace, use the shortcut:
**`Shift` + `Alt` + `B`**

This will open the **Trace Bitmap** (Vetorizar) panel on the right side of the screen.

---

## 3. Adjusting the Brightness Threshold
The "Brightness Threshold" (Limiar de Brilho) determines how the software distinguishes between the background and the lines of your image.

1.  **Preview:** Check the **Live Updates** (Atualizações automáticas) box to see the changes in real-time.
2.  **Adjust:** Increase or decrease the **Threshold** value until the black areas in the preview represent exactly what you want the laser to process.
3.  **Apply:** Click **Apply** (Aplicar).

[Image: Adjusting the brightness threshold slider]

---

## 4. Finalizing the Vector
After clicking Apply, the software creates a vector version on top of your original image.

1.  **Separate:** Click and drag the new vector to the side.
2.  **Cleanup:** Select the original pixel image (the one that looks "blurry" when you zoom in) and delete it.
3.  **Verify:** Your new file is now a vector! You can change its size without losing quality and move it to a Cutting or Engraving layer.

<figure markdown="span">
  ![](/assets/images/construcao-light.png#only-light){ width="400" }
  ![](/assets/images/construcao-dark.png#only-dark){ width="400" }
  <figcaption>Figure 1: Original pixel image vs. the new clean vector path (Coming Soon)</figcaption>
</figure>

---

!!! success "Pro Tip: Contrast is Key"
    The vectorization tool works best with high-contrast images (black and white). If your image has very light colors, try increasing the **Brightness Threshold** to make sure the software captures all the details.

---
**Let's Neon It!**
Vectors are essential for clean cuts. If your image is too complex to vectorize automatically, contact **Neon Laser Support**—we can help you optimize your files for the best result.