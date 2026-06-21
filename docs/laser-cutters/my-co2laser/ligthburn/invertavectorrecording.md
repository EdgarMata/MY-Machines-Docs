# How to Invert a Vector Engraving

Inverting a vector engraving in LightBurn is a simple process once you understand how the software calculates "fills".

## The Concept of Fills
LightBurn determines what to fill based on closed shapes (continuous loops). 
* **Single Closed Shape**: The laser engraves everything inside that shape.
* **Nested Closed Shapes**: When you place one closed shape inside another on the same layer, LightBurn toggles the fill. Instead of filling everything, it only engraves the space **between** the outlines.

## How to Invert Your Design
To invert a graphic, you simply need to place an outline around it:
1. **Create an Outline**: Draw a shape (like a rectangle or circle) around the graphics you want to invert.
2. **Same Layer**: Ensure both the original graphic and the new outline are assigned to the **same Fill layer**.
3. **Result**: The area that was previously empty will now be engraved, and your original shapes will remain as "islands" of unengraved material.

## Using the Offset Tool
One of the quickest ways to create an organic outline around your shapes is by using the **Offset Tool**:
* **Distance**: Specify how far the outline should be from your original shape.
* **Corner Style**: Choose between rounded, beveled, or sharp corners.
* **Selection**: You can choose to offset all shapes or just the outer ones.

## Important Requirements
* **Closed Shapes Only**: This process only works with closed shapes. Open shapes (where start and end points do not meet) cannot be filled.
* **Avoid Layer Mismatch**: If the outline and the graphic are on different layers, the laser will engrave both entirely, leading to overlapping areas being engraved twice instead of inverting.

---
*Source: LightBurn Software Official Tutorials*