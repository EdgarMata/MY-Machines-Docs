# Guide to the Perfect First Layer

!!! quote
    The first layer is not just a layer; it's the foundation of your entire print. A perfect first layer means 90% of the battle is won.

A poorly executed first layer is the number one cause of failed prints. Adhesion problems, lifted corners (warping), and "spaghetti" almost always start here. Follow these steps to ensure a solid base.

### 1. Bed Leveling

The goal is to ensure that the distance between the nozzle and the print bed is exactly the same at all points.

!!! tip "The Paper Method (Manual Leveling)"
    1.  Heat the bed and nozzle to your usual printing temperatures (e.g., 200°C/60°C for PLA). Materials expand with heat, so leveling cold is inaccurate.
    2.  Disable the stepper motors ("Disable Steppers").
    3.  Move the print head to each of the four corners of the bed.
    4.  Place a sheet of 80g/m² paper between the nozzle and the bed.
    5.  Adjust the leveling screw for that corner until you feel slight resistance when pulling the paper. The paper should scrape the nozzle but not get stuck.
    6.  Repeat the process for all four corners at least twice, as adjusting one corner slightly affects the others.

If you have **Automatic Bed Leveling (ABL)**, make sure the sensor is working correctly and run the leveling routine with the bed already hot.

### 2. Z-Offset Calibration

The Z-Offset is the fine distance between the "zero" position of the ABL sensor (or Z endstop) and the actual position where the nozzle touches the bed. It's the most critical adjustment for "squishing" the first layer just right.

![Z-Offset examples](https://i.imgur.com/3qA3f9R.png)

* **Too High:** The filament is deposited in the air. The lines don't touch and don't stick to the bed.
* **Too Low:** The nozzle drags on the bed, the filament can't come out or comes out translucent. Risk of scratching the bed and clogging the nozzle.
* **Perfect:** The filament lines are slightly flattened and fuse perfectly with each other, with no gaps or ridges.

### 3. Temperature and Speed

!!! success "The Slow and Hot Rule"
    For the first layer, use slightly higher temperatures and much lower speeds than for the rest of the print.

* **Temperature:** Add 5°C to 10°C to your normal nozzle and bed temperature for the first layer. This makes the plastic more fluid and the bed more "sticky."
* **Speed:** Set the first layer speed in your slicer to a low value, like **15mm/s to 20mm/s**. This gives the plastic time to melt, adhere, and settle properly.

### 4. Clean Surface

Impressões digitais, pó e resíduos são inimigos da adesão.

* Limpe a sua base de impressão regularmente com **Álcool Isopropílico (IPA)** com concentração superior a 90%.
* Se a adesão diminuir drasticamente, lave a base com **água morna e sabão da loiça** para remover óleos e resíduos mais teimosos. Seque bem sem tocar na superfície de impressão.

### Checklist da Primeira Camada Perfeita

- [ ] A base e o bico estão pré-aquecidos?
- [ ] A base foi nivelada (manualmente ou por ABL)?
- [ ] O Z-Offset está calibrado para um "esmagamento" perfeito?
- [ ] A velocidade da primeira camada está definida para ≤ 20mm/s?
- [ ] A temperatura da primeira camada está 5-10°C acima do normal?
- [ ] A superfície de impressão está limpa e livre de gordura?