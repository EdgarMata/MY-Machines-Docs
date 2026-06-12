
O arrefecimento da peça (Part Cooling) é um dos aspetos mais subestimados na impressão 3D. Um fluxo de ar direcionado e potente solidifica o filamento assim que ele sai do bico, sendo crucial para obter detalhes nítidos e geometrias complexas.

!!! abstract "Qual o objetivo do arrefecimento?"
    O objetivo da ventoinha de arrefecimento da peça **não é arrefecer o bico**, mas sim o plástico que **acabou de ser extrudido**. Isto permite que a camada seguinte seja depositada sobre uma base sólida, evitando deformações.

### Problemas Causados por Mau Arrefecimento
* **Overhangs Caídos (Droopy Overhangs):** As camadas em ângulos acentuados não solidificam a tempo e curvam para baixo.
* **Pontes Deformadas (Bad Bridging):** As linhas de uma ponte não solidificam esticadas e caem.
* **Detalhes Empastelados:** Em camadas pequenas e rápidas, o calor acumula-se, derretendo os detalhes.
* **Curling e Deformação:** Cantos agudos de uma peça podem curvar para cima por falta de arrefecimento rápido.


=== "Modificações de Hardware"

    A forma mais eficaz de melhorar o arrefecimento é através de upgrades físicos.

    ### 1. Imprimir um Novo Fan Duct

    O "fan duct" (duto de ar) que vem de fábrica em muitas impressoras é ineficiente, soprando ar de forma pouco direcionada.

    !!! tip "Solução"
        Procure em sites como **Printables.com** ou **Thingiverse.com** por dutos de ar otimizados para o seu modelo de impressora. Designs populares como o **Satsana**, **Petsfang** ou **Hero Me** oferecem um fluxo de ar de 360° ou bilateral, melhorando drasticamente o desempenho.

    ### 2. Upgrade da Ventoinha

    Se o duto melhorado não for suficiente, pode trocar a ventoinha por uma mais potente.

    !!! info "Ventoinhas 5015 Blower"
        A ventoinha "5015 Blower Fan" é um upgrade comum. Gera uma pressão de ar muito superior às ventoinhas axiais ou "blowers" de 4010 que vêm de fábrica, resultando num arrefecimento muito mais eficaz. Verifique a voltagem (12V ou 24V) da sua impressora antes de comprar.

=== "Ajustes de Software (Slicer)"

    Pode melhorar muito o arrefecimento apenas com as definições do seu slicer.

    ### 1. Velocidade da Ventoinha (Fan Speed)

    * **PLA:** Requer o máximo de arrefecimento. Defina a ventoinha para **100%** após as primeiras 2-3 camadas.
# Optimizing Cooling for Better Prints

Part cooling is one of the most underestimated aspects of 3D printing. A directed and powerful airflow solidifies the filament as soon as it leaves the nozzle, which is crucial for sharp details and complex geometries.

!!! abstract "What is the goal of cooling?"
    The goal of the part cooling fan is **not to cool the nozzle**, but rather the plastic that has **just been extruded**. This allows the next layer to be deposited on a solid base, preventing deformations.

### Problems Caused by Poor Cooling
* **Droopy Overhangs:** Layers at steep angles do not solidify in time and droop down.
* **Bad Bridging:** Bridge lines do not solidify stretched and sag.
* **Muddy Details:** On small and fast layers, heat accumulates, melting details.
* **Curling and Warping:** Sharp corners of a part may curl up due to lack of rapid cooling.

---

=== "Hardware Modifications"

    The most effective way to improve cooling is through physical upgrades.

    ### 1. Print a New Fan Duct

    The stock fan duct on many printers is inefficient, blowing air in an unfocused way.

    !!! tip "Solution"
        Search sites like **Printables.com** or **Thingiverse.com** for optimized air ducts for your printer model. Popular designs like **Satsana**, **Petsfang**, or **Hero Me** offer 360° or bilateral airflow, drastically improving performance.

    ### 2. Fan Upgrade

    If the improved duct is not enough, you can swap the fan for a more powerful one.

    !!! info "5015 Blower Fans"
        The "5015 Blower Fan" is a common upgrade. It generates much higher air pressure than the stock axial or 4010 blower fans, resulting in much more effective cooling. Check your printer's voltage (12V or 24V) before buying.

=== "Software (Slicer) Adjustments"

    You can greatly improve cooling just with your slicer settings.

    ### 1. Fan Speed

    * **PLA:** Requires maximum cooling. Set the fan to **100%** after the first 2-3 layers.
    * **PETG:** Requer menos arrefecimento para garantir uma boa adesão entre camadas. Use entre **30% a 50%**.
    * **ABS/ASA:** **Nenhum arrefecimento.** A ventoinha deve estar a **0%**. Arrefecimento rápido causa fissuras e "warping".

    ### 2. Tempo Mínimo por Camada (Minimum Layer Time)

    !!! success "Definição Essencial para Detalhes"
        Esta definição (encontrada em "Cooling" no seu slicer) força a impressora a abrandar em camadas muito pequenas. Se uma camada demorar menos que o tempo mínimo definido (ex: 10 segundos), a impressora reduz a velocidade para garantir que a camada anterior tem tempo de solidificar antes de receber a próxima.

    ### 3. Definições de Ponte (Bridging Settings)

    A maioria dos slicers tem uma secção dedicada a pontes. Aí pode definir a velocidade da ventoinha para **100%** apenas durante a execução de pontes, mesmo que esteja a usar um material como PETG que normalmente requer menos arrefecimento.
