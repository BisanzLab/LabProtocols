# qPCR-based detection and quantification of bacteria

## Materials and Equipment

- [ ] iTaq™ Universal Probes Supermix (BioRad 1725132)
- [ ] CFX384 thermocycler (Biorad)
- [ ] 384 Plates for qPCR (Biorad #HSP3865)
- [ ] Optically clear Plate Seals (Biorad Microseal ‘B’ #MSB1001)
- [ ] 10x Assay mix (prepare 2µM of each oligo below in nuclease-free water)
- [ ] 10-fold dilution series of gDNA (from any bacteria). Use the QuBit DNA concentration to calculate 16S copy number based on [genome size to genome copy number](http://nebiocalculator.neb.com/#!/dsdnaamt) and [rRNA copy number](https://rrndb.umms.med.umich.edu/). For example: 1ng of <i>E. lenta</i> DSM 2243 DNA ~ 2.7E5 genome copies and the 16S rRNA copy number is 3, so the first point on a 10-fold dilution series prepared from 10ng/µL gDNA is 8.1E5 16S rRNA copies/µL. Alternatively a full length 16S rRNA amplicon an be used instead for the standard but be sure to dilute to at least 1e8 copies/ul before loading on standard curve.
- [ ] Extracted gDNA and knowledge of the original weight/volume extracted and the final elution volume. Check the gDNA using a nanodrop and if there is any indiciation of suspected ethanol carryover, dilute all samples 10x before running.


#### Oligos
|Oligo|Sequence|Stock [µM]|Working [µM]|Final [nM]|
|-|-|-|-|-|
|891F|TGGAGCATGTGGTTTAATTCGA|100|2|200|
|1003R|TGCGGGACTTAACCCAACA|100|2|200|
|1002P|	 	[6FAM]CACGAGCTGACGACARCCATGCA[BHQ1]|100|2|200|

***

## Setting up qPCR RXNs

The master mix we are using has an antibody-mediated hot-start, and as such can be set up at RT in the PCR flow-hood in a 384 well plate. If quantification is desired, the reactions should be set up in triplicate.

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
Anneal/Extend | 60˚C	| 15 sec
||
Hold	| 4˚C	Hold | 0 sec

When setting up the plate using the BioRad software, select the 384 plate template with all channels (not the FAM/SYBR only). Using the plate editor, change your standard curves from unknown, to standards and enter the copy number you have calculated.

### Interpretation

To convert from the assay concentration to the 16S copy per gram or mL it is essential to know the original mass/volume that was extracted. Assuming the DNA was extracted from 100 mg of feces and the final elution volume during the DNA extraction was 50 ul, and a 10x dilution was performed before the assay see below:

5e8 16S copies/ul (from qPCR assay) * (50 ul elution volume / 4 ul template in rxn) * (10 Xdilution) / (0.1g) = 6.2e11 16S copies/g.

