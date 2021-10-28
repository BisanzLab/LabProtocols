# qPCR-based detection and quantification of *C. difficile TcdB*

## Materials and Equipment

- [ ] iTaq™ Universal Probes Supermix (BioRad 1725132)
- [ ] CFX384 thermocycler (Biorad)
- [ ] 384 Plates for qPCR (Biorad #HSP3865)
- [ ] Optically clear Plate Seals (Biorad Microseal ‘B’ #MSB1001)
- [ ] 10x Assay mix (prepare 2µM of each oligo below in nuclease-free water)
- [ ] 10-fold dilution series of gDNA (from a TcdB+ *C. difficile*). Use the QuBit DNA concentration to calculate genome copy number based on [genome size to genome copy number](http://nebiocalculator.neb.com/#!/dsdnaamt). For example: 2.1ng of <i>C. difficile</i> 630 ~ 5.5E5 genome copies = 5.5e5 TcdB copies.
- [ ] Extracted gDNA and knowledge of the original weight/volume extracted and the final elution volume. Check the gDNA using a nanodrop and if there is any indiciation of suspected ethanol carryover, dilute all samples 10x before running.


#### Oligos
|Oligo|Sequence|Stock [µM]|Working [µM]|Final [nM]|
|-|-|-|-|-|
|TcdB_F|TACAAACAGGTGTATTTAGTACAGAAGATGGA|100|2|200|
|TcdB_R|CACCTATTTGATTTAGMCCTTTAAAAGC|100|2|200|
|1002P|[6FAM]TTTKCCAGTAAAATCAATTGCTTC[BHQ1]|100|2|200|

***

## Setting up qPCR RXNs

The master mix we are using has an antibody-mediated hot-start, and as such can be set up at RT in the PCR flow-hood in a 384 well plate.

### Reaction mixture

|Component|[stock]|µL/rxn|[final]|
|-|-|-|-|
|iTaq Supermix|2X|5|1X|
|10X assay mix|2µM|1|200nM|
|DNA template|variable|4|varable|

After setting up the plate, breifly centrifuge to mix and remove air bubbles before transfering to the CFX384.

### Cycling Parameters

Cycle |	Temperature (˚C)  | Time
------|-------------------|------
Initial Denaturation   |	95	| 5min
||
40 cycles:
Denature | 95˚C | 5 sec
Anneal/Extend | 56.6˚C	| 15 sec
||

When setting up the plate using the BioRad software, select the 384 plate template with all channels (not the FAM/SYBR only). Using the plate editor, change your standard curves from unknown, to standards and enter the copy number you have calculated.

### Interpretation

To convert from the assay concentration to the genome copies per gram or mL it is essential to know the original mass/volume that was extracted. Assuming the DNA was extracted from 100 mg of feces and the final elution volume during the DNA extraction was 50 ul, and a 10x dilution was performed before the assay see below:

5e5 TcdB copies/ul (from qPCR assay) * (50 ul elution volume / 4 ul template in rxn) * (10 Xdilution) / (0.1g) = 6.25e8 GE/g.
