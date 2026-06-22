# Replacing the Nozzle

Nozzles are consumable parts. They wear out over time, and this wear can accelerate dramatically when printing with abrasive filaments (like carbon fiber, glow-in-the-dark, or wood-fill). A worn nozzle can cause a loss of detail and extrusion issues.

!!! danger "Hot-Tightening is CRITICAL"
    You must perform the final tightening of the nozzle while the hotend is at a high temperature. Metal expands when heated. Tightening the nozzle when hot ensures it forms a perfect seal against the heatbreak inside the heater block. **Failing to do this will cause molten plastic to leak out from the threads, creating a massive mess and potentially damaging your hotend.**

### Replacement Procedure

1.  **Preheat**: In the web interface, heat the hotend to a high temperature, such as **250°C**. This ensures any hardened plastic inside is molten and allows the metal parts to expand.
2.  **Support the Heater Block**: Use an adjustable wrench or a correctly sized spanner to grip and hold the heater block steady. It is critical that you **do not** allow the block to twist, as this can damage the wires or break the heatbreak.
3.  **Remove Old Nozzle**: While holding the heater block, use a socket wrench or the correct spanner to unscrew and remove the old nozzle. Remember, it is extremely hot. Place it on a heat-resistant surface.

<figure markdown="1">
  ![Removing an old nozzle while holding the heater block](/images/image-placeholder.png#only-light){ width="700" }
  ![Removing an old nozzle while holding the heater block](/images/image-placeholder.png#only-dark){ width="700" }
  <figcaption>A wrench holding the heater block steady while a socket wrench is used to unscrew the hot nozzle.</figcaption>
</figure>

4.  **Install New Nozzle**: While the hotend is still hot, carefully screw in the new nozzle by hand until it is finger-tight. Be careful not to cross-thread it. It should not screw all the way in; a small gap between the nozzle hex and the heater block is normal.
5.  **Hot-Tighten**: While still holding the heater block steady with the wrench, use your socket wrench to give the new nozzle a final tightening. This should be about a quarter-turn past finger-tight. It needs to be snug and secure, not excessively torqued.
6.  **Re-Calibrate Z-Offset**: A new nozzle may have a slightly different length. After replacement, you **must** re-run your Z-offset calibration to ensure the correct first-layer height.