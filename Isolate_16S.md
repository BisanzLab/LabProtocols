# Pure culture isolate DNA extraction and 16S rRNA sequencing protocol
## Version 1.2: 13 Dec, 2021

***

## 1. Scope and Principle
This protocol is intended for the identification of pure culture isolates from an agar plate or broth culture. Genomic DNA is extracted in a quick and dirty way using Instagene (Biorad) although any genomic isolation prep could be used instead. PCR is then performed, purified and sent for paired Sanger sequencing.

## 2. Materials
- [ ] Instagene Matrix (Biorad #732-6030)
- [ ] Wide bore 200 µL pipette tips (or clean scissors to cut tip off end of normal tip)
- [ ] 1.5 mL nuclease-free microcentrifuge tubes
- [ ] nuclease-free water or PBS
- [ ] 200 µL PCR tubes
- [ ] Waterbath/heatblock/PCR thermocycler capable of 56˚C and 100˚C
- [ ] Amplitaq Gold 360 Master Mix (Life Tech/Thermofisher 4398881)
- [ ] 2µM 8F (pA) primer (5-AGAGTTTGATCCTGGCTCAG-3)
- [ ] 2µM 1542R (pH) primer (5- AAGGAGGTGATCCAGCCGCA-3)
- [ ] Purelink PCR purification kit (Life Technologies #K3100-01; or Qiagen equivalent)
- [ ] (optional) 2µM 515F primer (5-GTGYCAGCMGCCGCGGTAA-3)
- [ ] (optional) 2µM 806RB primer (5-GGACTACNVGGGTWTCTAAT-3)
- [ ] (optional) AMPure XP bead (Beckman coulter A63881)
- [ ] (optional) Freshly prepared 70% EtOH
- [ ] (optional) Magnetic capture plate

***
## 3. DNA Extraction
- [ ] Pick a single colony from a freshly prepared culture plate and resuspend
in 1mL of PBS or sterile H2O in a microcentrifuge tube **OR** Transfer 200ul from a broth culture to a microcentrigue tube.
- [ ] Centrifuge at ~10,000 xg for 1 minute.
- [ ] Remove the supernatant and resuspend in 100 µL of Instagene matrix (matrix should be well mixed and use wide bore tips)
- [ ] Mix thoroughly by vortexing
- [ ] Incubate at 56˚C for 30 minutes
- [ ] Mix thoroughly by vortexing
- [ ] Incubate at 100˚C for 8 minutes
- [ ] Mix thoroughly by vortexing
- [ ] Centrifuge for 3 minutes at max (~16,000 xg)
- [ ] Transfer 60 µL of the supernatant containing gDNA to a new
microcentrifuge tube. This is optional and supernatant can be used directly for PCR.
- [ ] Store gDNA at -20˚C for long term storage or 4˚C for short term.

***
## 4. PCR

- [ ] Prepare a master mix for PCR as outlined in Table 4.1.
- [ ] Add 1 µL of gDNA for a total reaction volume of 20 µL. Be sure to include a reaction with 1 µL of H2O as no template control (NTC).
- [ ] Pop spin to remove any air bubbles.
- [ ] Run the PCR using the PCR cycle parameters indicated in Table 4.2

##### Table 4.1 PCR Master Mix
Component	| Stock Concentration | Final Concentration | per 50µL rxn
----------|---------------------|---------------------|-------------
Amplitaq Gold | 2x | 1x | 10 µL
Water | - | - | 4 µL
8F | 2µM | 400 nM | 2 µL
1542R | 2µM | 400nM | 2 µL
gDNA | variable | variable | 1µL
**Total** | | | **20 µL**

##### Table 4.2 PCR Cycles
Cycle |	Temperature (˚C)  | Time
------|-------------------|------
Initial Denaturation   |	95	| 10 min
30 cycles:
Denature | 95˚C | 30 sec
Anneal | 55˚C	| 30 sec
Extend | 72˚C | 60 sec
Holding	| 4˚C	Hold | 0 sec


***
## 5. Reaction cleanup

#### Option A: AMPure XP beads
This protocol works better for a large number of samples being processed.
- [ ] Add 18 µL AMPure XP beads (make sure well suspended) to 20 µL PCR reaction (0.9x volume beads)
- [ ] Mix by pipetting and capture for ~5 min on magnetic rack
- [ ] Keeping tubes on magnetic rack, remove supernatant and replace with 200 µL fresh 70% ethanol.
- [ ] Keeping tubes on magnetic rack, remove supernatant and replace with 200 µL fresh 70% ethanol.
- [ ] Keeping tubes on magnetic rack, remove supernatant and replace with 200 µL fresh 70% ethanol.
- [ ] Keeping tubes on magnetic rack, remove supernatant.
- [ ] Pop spin to bring down any ethanol on the sides. Capture on stand.
- [ ] Use 10µL pipette to remove any trace EtOH on bottom of rack.
- [ ] Air dry ~10 min.
- [ ] Add 30 µL water and pipette to mix. This step elutes the DNA off the beads. Capture on magnetic rack ~2-5 minutes.
- [ ] Remove 25 µL of eluted DNA to fresh tube and discard bead tubes.


#### Option B: Purelink PCR cleanup
If only a few samples are being processed this will be faster. The Qiagen PCR cleanup kit can be used interchangeably with the same protocol and volumes.
- [ ] Add 200 µL of buffer B2 to 50 µL of the reaction (4 volumes).
- [ ] Transfer 250 µL of the mixture to a spin column and centrifuge at maximum speed for 1 minute.
- [ ] Discard flow through and add 650 µL of wash buffer W1. Centrifuge at maximum speed for 1 minute.
- [ ] Discard flow through and recentrifuge for 3 minutes.
- [ ] Transfer spin column to fresh nuclease free microcentrifuge tube and add 50 µL of Elution buffer (Tris-HCl, TE, H2O will all work as well).
- [ ] Incubate at room temperature for 1 minute and then centrifuge for 2 minutes at maximum speed.
- [ ] Dispose of spin column and keep eluted DNA.

***
## 6. QC
- [ ] Use a nanodrop or qubit to quantify products as well as NTC. Yield per this protocol should yield ~20-40 ng/µL product with <2 ng/µL in the NTC.
- [ ] Dilute PCR products to 10 ng/µL
- [ ] (optional) Prepare and run a 1% agarose gel using TAE or TBE buffer using 10 µL of PCR reaction. Confirm presence of ~1,500 bp band and the absence of product in the NTC.

***
## 7. Sequencing
**TBD**


***
## 8. Cleaning and interpreting sequence
- [ ] When sequence results are available (usually next day), download **.ab1** files.
- [ ] Using [4 Peaks](https://nucleobytes.com/4peaks/index.html) (mac) or [FinchTV](http://jblseqdat.bioc.cam.ac.uk/gnmweb/download/soft/FinchTV_1.4/doc/) (windows) trim trace to remove any Ns, resolving them by manually inspecting the electropherogram where possible.
- [ ] Overlap sequences using a program such as [CAP3](http://doua.prabi.fr/software/cap3).
- [ ] [Nucleotide BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome) against NCBI nr and NCBI 16S reference sequences excluding matches to uncultured material.
- [ ] A species level identification should involve a >97% match over the entire length of the product to a defined species. If there are multiple equal matches (for example to <i>Lactobacillus casei</i>, and <i>Lactobacillus rhamnosus</i>), it will not be possible to resolve the species from 16S rRNA alone. Try excluding the species your top hit is against and see the nearest match.
