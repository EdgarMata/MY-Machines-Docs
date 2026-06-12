# How to Prevent Warping

"Warping" happens when the corners of a 3D print lift and detach from the print bed during the process. It's a physical problem caused by the thermal contraction of plastic.

!!! quote "The Physics of Warping"
    When plastic is extruded, it's hot. As it cools, it contracts. The upper layers cool faster and, as they contract, pull on the lower layers, generating a force that lifts the corners of the part from the bed. Materials like **ABS** contract much more than **PLA**.

### Solutions Focused on Bed Adhesion

The first line of defense is to ensure the first layer is perfectly stuck to the bed.

1.  **Impeccably Clean Bed:** Use isopropyl alcohol (IPA) before every print.
2.  **Perfect First Layer:** Follow the [perfect first layer guide](./perfect-first-layer.md) to ensure ideal "squish."
3.  **Correct Bed Temperature:** Keeping the bed hot (e.g., 60°C for PLA, 100°C for ABS) keeps the first layers above their "glass transition temperature," reducing the urge to contract.
4.  **Adhesion Helpers (Brims and Rafts):**

    === "Brim"
        A "brim" is a series of concentric lines printed around the base of your part.
        * **Function:** Drastically increases the surface area of the first layer, giving much more "grip power" to the part.
        * **Ideal Use:** The best choice in most cases. Easy to remove and uses little extra material.

    === "Raft"
        A "raft" is a thick grid printed underneath your entire part. Your part is printed on top of this disposable raft.
        * **Function:** Creates a new, perfectly flat print surface with good adhesion, combating an uneven bed or severe adhesion problems.
        * **Ideal Use:** For very small parts with little contact area or when printing with very difficult materials like ABS on an open printer.

### Solutions Focused on Ambient Temperature

The second line of defense is to minimize contraction by controlling cooling.

1.  **Use an Enclosed Printer:** This is the **most effective solution** for materials like ABS, ASA, or Nylon. An enclosure keeps the air temperature around the part high and stable, drastically reducing contraction.
2.  **Turn Off the Cooling Fan:** For the first 5 to 10 layers, turn off the part cooling fan completely. This gives the base of the part time to cool slowly and evenly.
3.  **Use a "Draft Shield":** Most slicers have this option. It prints a thin perimeter wall around the entire part, rising with it. This wall protects the part from cold drafts, acting as an improvised enclosure.