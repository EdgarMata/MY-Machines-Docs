
A velocidade de impressão é mais do que um único número. É um ecossistema de definições que interagem entre si e com os limites físicos da sua impressora. O objetivo não é imprimir o mais rápido possível, mas sim o mais rápido possível *mantendo a qualidade desejada*.

!!! info "Os Compromissos da Velocidade"
    * **Velocidade vs. Qualidade da Superfície:** Velocidades mais altas causam mais vibrações, resultando em "ghosting" e detalhes menos nítidos.
    * **Velocidade vs. Resistência da Peça:** Velocidades muito altas podem levar a uma fusão inadequada entre camadas, resultando em peças mais fracas.
    * **Velocidade vs. Precisão Dimensional:** Com velocidades altas, a pressão no bico flutua mais, o que pode afetar a precisão das dimensões da peça.

### O Ecossistema de Velocidades no Slicer

Não existe uma única "velocidade". O seu slicer controla várias:

* **Print Speed:** A velocidade base. As outras são muitas vezes uma percentagem desta.
* **Outer Wall Speed (Perímetro Exterior):** Deve ser mais lenta (ex: 50% da velocidade base) para garantir um acabamento superficial limpo e preciso.
* **Inner Wall Speed (Perímetros Interiores):** Pode ser mais rápida que a parede exterior, pois não é visível.
* **Infill Speed (Preenchimento):** Geralmente, a velocidade mais alta de todas. A sua aparência não importa.
* **Top/Bottom Speed:** Mais lenta, similar à parede exterior, para garantir um topo sólido e sem falhas.
* **Travel Speed (Velocidade de Viagem):** Deve ser o mais alta possível (ex: 150-200 mm/s) para reduzir o "stringing".
* **First Layer Speed (Velocidade da Primeira Camada):** Muito lenta (ex: 20 mm/s) para garantir a adesão.

### Limitações de Hardware que Definem a sua Velocidade

1.  **Hotend (Fluxo Volumétrico Máximo):** O seu hotend só consegue derreter uma certa quantidade de plástico por segundo. Este é o verdadeiro limite da sua velocidade e é medido em **mm³/s**. Tentar extrudir mais rápido que este limite resultará em "under-extrusion" (falta de material).
2.  **Sistema de Movimento (Vibrações):** A rigidez do chassis, o peso das partes móveis e a tensão das correias definem a que velocidade pode imprimir antes de o [ghosting](./reduce-vibration.md) se tornar inaceitável.

!!! success "Como encontrar o seu limite?"
    1.  **Teste de Fluxo Máximo:** Procure por "Max Flow Rate test" ou "Volumetric Flow test" no Printables. Estes modelos imprimem a velocidades crescentes para que possa ver em que ponto a extrusão começa a falhar.
    2.  **Aceleração e Jerk:** Para além da velocidade, a aceleração é fundamental. Uma máquina rígida com firmware avançado (como Klipper com "Input Shaping") pode usar acelerações muito mais altas, reduzindo o tempo de impressão drasticamente sem sacrificar a qualidade.

Em resumo, comece com um perfil conservador (ex: 50-60mm/s para PLA) e aumente gradualmente a velocidade do preenchimento e dos perímetros interiores, mantendo as paredes exteriores lentas para garantir a qualidade.
# Optimizing Print Speed: Balancing Speed and Quality

Print speed is more than a single number. It's an ecosystem of settings that interact with each other and with the physical limits of your printer. The goal is not to print as fast as possible, but as fast as possible *while maintaining the desired quality*.

!!! info "Speed Trade-offs"
    * **Speed vs. Surface Quality:** Higher speeds cause more vibrations, resulting in ghosting and less sharp details.
    * **Speed vs. Part Strength:** Very high speeds can lead to poor layer bonding, resulting in weaker parts.
    * **Speed vs. Dimensional Accuracy:** At high speeds, pressure in the nozzle fluctuates more, which can affect the accuracy of part dimensions.

### The Speed Ecosystem in the Slicer

There is no single "speed." Your slicer controls several:

* **Print Speed:** The base speed. Others are often a percentage of this.
* **Outer Wall Speed:** Should be slower (e.g., 50% of base speed) to ensure a clean, precise surface finish.
* **Inner Wall Speed:** Can be faster than the outer wall, since it's not visible.
* **Infill Speed:** Usually the highest speed. Its appearance doesn't matter.
* **Top/Bottom Speed:** Slower, similar to the outer wall, to ensure a solid, flawless top.
* **Travel Speed:** Should be as high as possible (e.g., 150-200 mm/s) to reduce stringing.
* **First Layer Speed:** Very slow (e.g., 20 mm/s) to ensure adhesion.

### Hardware Limitations That Define Your Speed

1.  **Hotend (Maximum Volumetric Flow):** Your hotend can only melt a certain amount of plastic per second. This is the true speed limit and is measured in **mm³/s**. Trying to extrude faster than this will result in under-extrusion.
2.  **Motion System (Vibrations):** The rigidity of the frame, the weight of moving parts, and belt tension define how fast you can print before [ghosting](./reduce-vibration.md) becomes unacceptable.

!!! success "How to Find Your Limit?"
    1.  **Max Flow Rate Test:** Search for "Max Flow Rate test" or "Volumetric Flow test" on Printables. These models print at increasing speeds so you can see at what point extrusion starts to fail.
    2.  **Acceleration and Jerk:** Besides speed, acceleration is key. A rigid machine with advanced firmware (like Klipper with "Input Shaping") can use much higher accelerations, drastically reducing print time without sacrificing quality.

In summary, start with a conservative profile (e.g., 50-60mm/s for PLA) and gradually increase infill and inner wall speeds, keeping outer walls slow to ensure quality.