# Pillowing

!!! abstract "The Problem"
    **Pillowing** occurs when the top solid layer of a print does not form correctly over the infill structure. Instead of a smooth, flat surface, you get a lumpy surface with gaps, holes, or a "pillow-like" appearance.

<figure markdown="1">
  ![The top surface of a 3D print showing pillowing](/images/image-placeholder.png#only-light){ width="600" }
  ![The top surface of a 3D print showing pillowing](/images/image-placeholder.png#only-dark){ width="600" }
  <figcaption>The top solid surface of a 3D print showing bumps, gaps, and an uneven finish, a defect known as pillowing.</figcaption>
</figure>

## Common Causes and How to Fix Them

Pillowing is essentially a bridging problem that happens across the entire top surface. The first few solid top layers have to bridge the gaps in the infill pattern. If these "bridges" fail, the problem occurs.

### 1. Insufficient Number of Top Layers

This is the most common cause. If you have too few solid top layers, they don't have enough thickness to completely cover the gaps from the first failed bridges over the infill.

* **Solution:** Increase the number of `Top Solid Layers` in your slicer. If you are using 3 or 4, try increasing to **5 or 6**. For lower layer heights (e.g., 0.12mm), you might need 7 or 8. A good rule of thumb is to have a total top thickness of at least 0.8mm to 1.0mm.

### 2. Infill Density Too Low

If the infill percentage is very low (e.g., <15%), the gaps that the top layers have to bridge are huge, making bridging very difficult.

* **Solution:** Increase the `Infill Density`. A value of **20% to 25%** is generally a good balance between strength, print time, and a solid foundation for the top layers.

### 3. Insufficient Cooling or High Temperature

Just like with bridging, if the filament is too hot or not cooled quickly, the lines of the first top layer will sag into the infill instead of forming a straight bridge.

* **Fix 1:** Ensure your part cooling fan is running at an appropriate speed (100% for PLA) when printing the top layers.
* **Fix 2:** Slightly lower the printing temperature. Less heat means the plastic solidifies faster.

### 4. Infill Pattern

Some infill patterns provide more support than others.

* **Solution:** Patterns like `Grid`, `Cubic`, or `Gyroid` offer good, multi-directional support for the top layers. If you're using a pattern like `Lines`, ensure the slicer prints it so that the lines of the first top layer are not parallel to the infill lines below.

## Quick Checklist
- [ ] Increase the number of `Top Solid Layers` to 5 or more.
- [ ] Increase the `Infill Density` to at least 20%.
- [ ] Check that the cooling fan is working correctly on the top layers.
- [ ] Lower the printing temperature by 5°C.
- [ ] Use an infill pattern like `Grid` or `Gyroid`.