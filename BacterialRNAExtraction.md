# RNA Extraction from Gram Positive Bacteria and/or Fecal Samples
## April 2021

# Background

This protocol is JEB's version of PSP's version of ENB's version of JEB's original 2013 RNA extraction protocol developed for difficult-to-lyse lactobacilli. It is generally useful for most gram-positive microbes and fecal samples. This protocol uses mechanical disruption to ensure even lysis, but a pre-incubation in mutanolysin (50U/mL) and lysozyme (20mg/mL) can be substituted if a bead disrupter is not available. The protocol is set up for all supplies ordered from Life Technologies including the Purelink columns and on-column DNaseI treatment which should be considered mandatory for samples for qPCR/RNAseq and gene expression experiments. It can be noted that these purelink products are lower-cost direct replacements for the Qiagen RNAeasy equivalents which can be directly substituted if necessary. It is recommended to extract >1e7 CFU of bacteria to ensure sufficient RNA recovery. Note that ~20ng-2ug are required for reverse transcription for qPCR, and 1-5µg for library prep. The expected yield is >20ug total in 30µL.

# Supplies

## Consumables:
- [ ] Trizol (Life Technologies Cat # 15596-018)
- [ ] PureLink RNA Mini Kit (Life Technologies Cat # 12183025)
- [ ] Purelink DNase Set (Life Technologies Cat # 12185010)
- [ ] 100% Ethanol
- [ ] Chloroform
- [ ] Lysing Matrix E (MPBio 116914050-CF)
- [ ] *Optional:* Bacterial RNA Protect (Qiagen Cat #76506)
- [ ] *Optional:* Molecular Grade 3M Sodium Acetate (Ambion #AM9740)
- [ ] *Optional:* RNAclean XP Beads or equivalent (Beckman #A63987)
- [ ] *Optional:* RNaze zap or equivalent (Sigma R2020-250ML)


## Equipment:
- [ ] Table top refrigerated centrifuge capable of spinning 15 mL tubes
- [ ] Table top microcentrifuge capable of spinning 1.5mL tubes >15,000g
- [ ] Bead Disrupter (ex Biospec Mini-beadbeater-96)
- [ ] *Optional:* magnetic capture plate.

***

# Protocol

## 1. Sample Preparation
*If sample is in liquid form, it is recommended to preserve the sample before centrifugation and flash freezing. Some organisms are particularly sensitive to centrifugation (ex. E. coli) and given that the half life of an mRNA is ~5min, the transcriptome can change considerably while the sample is in the centrifuge. Skip this step for solid samples: ex. feces.*
- [ ] Add 2 volumes Bacterial RNA protect to 1 volume bacterial culture. (ex 4mL RNA protect to 2mL culture).
- [ ] incubate mixture at RT for 5-10 minutes.
- [ ] Centrifuge at 5000xg for 5 minutes at 4˚C
- [ ] Flash freeze in liquid nitrogen and store at -80˚C until required. It is recommended to extract the sample within a month of freezing.

## 2. Extraction and DNAse treatment
- [ ] Clean workspace and pipettes using RNase Zap.
- [ ] Resuspend pellet/sample in 1mL TRIzol
- [ ] Transfer entire volume into lysing matrix E tube.
- [ ] Bead beat for 1 min and cool on ice for one minute. Repeat for a total of 3 minutes of bead beating.
- [ ] *Optional:* If there is significant debris in the tube, centrifuge for 5 minutes at 12,000xg and transfer the cleared supernatant to a fresh tube.
- [ ] Add 200µL chloroform, vortex for 15 seconds, and incubate at RT for 10 min
- [ ] Centrifuge for 15 min at 16,000xg at 4˚C.
- [ ] Transfer the upper clear aqueous phase (500µL) to a fresh 1.5mL tube.
- [ ] Add 500 µL 100% Ethanol and vortex to mix. Depending on yield you may observe the solution go cloudy at this step. *Note: 100% ethanol supposedly will keep all RNAs including small RNAs which may be desirable for RNAseq. If this is not desired, 70% ethanol may be used instead. Ethanol is also a more efficient precipitator than isopropanol thus increasing the yield*
- [ ] Transfer 500µL of new mixture to a purelink spin column and spin >12,000 g for 15 seconds, discard flow through.
- [ ] Repeat previous step to run entire mixture through spin column
- [ ] Add 350µL of wash buffer I to the spin column and centrifuge at >12,000xg for 15 seconds, discard flow through.
- [ ] Add 80 µL DNase mix (8µL 10x rxn buffer, 10µL DNase, 62µL RNase-free water). Incubate at RT for 15 min.
- [ ] Add 350µL of wash buffer I to the spin column and centrifuge at >12,000xg for 15 seconds, discard flow through.
- [ ] Move column to a new collection tube.
- [ ] Add 500µL wash buffer II (be sure that ethanol was added when the kit was first opened), centrifuge 15 seconds at >12,000xg, discard flow through.
- [ ] Repeat previous step.
- [ ] Centrifuge column for 1 min at >12,000xg to dry the column.
- [ ] Move the column to a collection tube and add 30 µL RNase-free water.
- [ ] Incubate at RT for 1 minutes.
- [ ] Centrifuge 1 minutes at >12,000xg and discard the column keeping the flow through containing your purified RNA.


# QC
Quality control can be accomplished in two ways. 1: Use a nanodrop to measure the concentration, 260/280, and 260/230 ratios. The concentration should ideally be >500ng/µL with a 260/280 > 1.8 and a 260/230> 1.4 which represents being free of proteins and salts/phenol respectively. If the sample is not clean, proceed with either of the protocols below. Ethanol precipitation is cheaper and will concentrate the sample, but takes longer. Bead capture is faster, requires less skill, but it more expensive.

Additionally, the samples can be analyzed for integrity by running a Bioanalyzer/Tapestation chip to ensure a the clear presence of the ribosomal peaks and the expected size distribution. Alternatively, a 1.5% agarose gel in TBE can be run which will allow for a crude approximation of quality. A denaturing gel is better for accessing RNA integrity, but is probably more hassle than it is worth.

***

# Ethanol Precipitation
*Recommended if samples need additional clean-up and/or concentration*.
- [ ] Add 1/10th volume (3µL) 3M sodium acetate and vortex briefly.
- [ ] Add 3 volumes (90µL) of 100% ethanol.
- [ ] *Optional:* Add 1µL of glycogen which may help with recovery of low yield samples. Should not be necessary for most higher biomass samples.
- [ ] Incubate at -20˚C overnight.
- [ ] Centrifuge 20 minutes at 16,000xg. Discard supernatant being careful not to disrupt pellet. *Sometimes the pellet will not be visible per se, just be very careful when loading hte tube into the centrifuge so you should know where the pellet is (ex: under the cap hinge).
- [ ] Add 500µL ICE COLD 70% ethanol (diluted from 100% ethanol in RNase-free water). Centrifuge 10 minutes at 16,000xg and discard supernatant.
- [ ] Add 500µL ICE COLD 70% ethanol (diluted from 100% ethanol in RNase-free water). Centrifuge 10 minutes at 16,000xg and discard supernatant.
- [ ] Briefly centrifuge to collect the last drops of ethanol and remove with fine pipette tip.
- [ ] Resuspend in desired volume of appropriate buffer.

***

# Bead Cleanup
*Recommended for high-throughput cleanups
- [ ] Add 1.8x volume (54µL) well-mixed beads to RNA and mix well.
- [ ] Incubate at RT for 5-minutes.
- [ ] Capture beads on stand until solution is clear and discard supernatant.
- [ ] Add 200µL freshly-prepared 70% ethanol, capture on stand, and discard supernatant.
- [ ] Repeat the above step for a total of 3x washes.
- [ ] Air dry the pellet for 10 minutes.
- [ ] Add 33µL nuclease-free water to elute RNA and mix well.
- [ ] Capture the beads and remove supernatant containing RNA to fresh tubes.
