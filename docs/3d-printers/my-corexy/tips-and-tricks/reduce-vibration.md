# Reducing Vibrations for Cleaner and Quieter Prints

Your 3D printer is a machine that moves its print head and/or bed at high speeds. These rapid movements and direction changes generate vibrations that affect print quality and produce noise.

!!! abstract "What is Ghosting / Ringing?"
    **Ghosting** (or "ringing") is a visual artifact that looks like ripples or ghostly echoes next to sharp corners or details in your print. It's caused by vibration in the printer's mechanical system that continues even after the print head has changed direction.

![Ghosting example](https://i.imgur.com/7H23bJ0.jpeg)

### Physical Solutions (The Foundation)

Physical stability is the first and most important step to reducing vibrations.

#### 1. A Solid and Stable Surface

!!! danger "Don't underestimate this!"
    Your printer should not be on a flimsy or unstable table (like an unmodified IKEA "Lack" table). Ideally, use a heavy workbench, a sturdy piece of furniture, or the floor. Any wobble in the surface will be transferred to your print.

#### 2. The Concrete Slab Trick

This is a popular and very effective community solution:

1.  Buy a concrete paving slab (e.g., 40x40cm).
2.  Place a dense foam mat or closed-cell foam under the slab.
3.  Put the printer on top of the slab.

The mass of the slab absorbs most high-frequency vibrations, and the foam isolates the slab from your table. The result is a drastic reduction in noise and ghosting.

#### 3. Anti-Vibration Feet

You can print feet that use squash balls or sorbothane blocks to absorb vibrations. These feet decouple the printer from the surface, reducing noise transmission.

#### 4. Mechanical Maintenance

- [ ] **Tighten the Belts:** Belts should be as tight as a bass guitar string. Not too much, but firm. Loose belts are a main cause of ghosting.
- [ ] **Check Wheels and Eccentrics:** Make sure all wheels running on aluminum extrusions are snug. There should be no wobble in the print head or bed. Adjust eccentric nuts as needed.
- [ ] **Firm Frame:** Check that all frame screws are tight.

### Software Solutions (Slicer and Firmware)

#### 1. Reduzir Velocidade e Aceleração

A forma mais simples de reduzir o "ghosting" é abrandar. No seu slicer, reduza os valores de:
* **Print Speed:** A velocidade geral.
* **Acceleration:** A rapidez com que a impressora atinge a velocidade máxima.
* **Jerk / Junction Deviation:** A rapidez com que a impressora pode mudar de direção.

Reduzir a aceleração é geralmente o mais eficaz.

#### 2. Input Shaping (A Solução Avançada)

!!! tip "O Futuro da Impressão Rápida"
    Firmwares modernos como o **Klipper** implementam uma técnica chamada "Input Shaping". Usando um acelerómetro barato (ADXL345) ligado temporariamente à cabeça de impressão, o firmware mede as frequências de ressonância exatas da sua máquina. Depois, altera os movimentos de forma inteligente para cancelar essas vibrações antes mesmo que elas aconteçam.

    Com o "Input Shaping" devidamente calibrado, é possível imprimir a velocidades extremamente altas (150mm/s ou mais) sem qualquer vestígio de "ghosting".