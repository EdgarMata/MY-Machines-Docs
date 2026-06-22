# Tips for Designing Your Own 3D Models

As you get more experienced, you might want to design your own parts. Keeping a few simple rules in mind during the design process will make your models much easier to print successfully.

---
### 1. Use Chamfers Instead of Fillets on Bottom Edges

* **Problem:** A rounded edge (a "fillet") on the bottom of a model creates a very steep overhang that is difficult for the printer to print cleanly. This often results in a messy, ugly surface.
* **Tip:** Whenever possible, use a straight 45-degree angle (a "chamfer") instead. A 45-degree angle is easy for any printer to handle and will result in a much cleaner bottom edge.

<figure markdown="1">
  ![Fillet vs Chamfer](/images/image-placeholder.png#only-light){ width="600" }
  ![Fillet vs Chamfer](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>Illustration comparing a 3D model with a rounded bottom edge (fillet) versus one with a 45-degree angled edge (chamfer).</figcaption>
</figure>

---
### 2. Split Complex Models into Multiple Parts

* **Problem:** A single, complex model might have overhangs in multiple directions, requiring a large amount of support material that is difficult to remove and leaves marks on the surface.
* **Tip:** It's often better to split a complex object into multiple, simpler parts that can each be oriented flat on the print bed. This drastically reduces the need for supports and improves the final surface quality. You can then glue the parts together after printing.

---
### 3. Design with Tolerances in Mind

* **Problem:** You design two parts that are meant to fit together (e.g., a peg and a hole), but after printing, they are too tight and won't fit.
* **Tip:** 3D printing is not perfectly precise. You must design a small gap, or "tolerance," between parts. A good starting point is to make the hole **0.2 mm to 0.3 mm** larger in diameter than the peg that goes inside it. For a very tight fit, you can try 0.1 mm. The best thing about 3D printing is that you can quickly print a small test piece to see which tolerance works best for your printer and material.