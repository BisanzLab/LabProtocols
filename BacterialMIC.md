# Bacterial Minimum Inhibitory Concentration (MIC) assay protocol

## Goal:
To determine the Minimum Inhibitory Concentration of anaerobic microbes versus compounds.

## Materials
- [ ] Sterile H2O, DMF, DMSO (Sigma **319937**)
- [ ] Syringe Filters (SFCA-Corning **431219**)
- [ ] 96 well culture plates (Falcon **351177**)
- [ ] 16 mL glass culture tubes (VWR **53283-802**)
- [ ] 2 mL Screw Top Tubes (VWR **10011-614**)
- [ ] Appropriate Liquid and Solid Media (Typically BHI-CHAVR or BHI-CHVR)
- [ ] 200 uL pipette tips (USA Scientific **1120-8710**)
- [ ] 10 uL pipette tips (USA Scientific **1120-3710**)
- [ ] 50 mL reservoirs (USA Scientific **1930-2530**)
- [ ] Spectrophotometer (VWR **10145-568**)
- [ ] Plate Reader (Thermo Fisher **A51119500C**)

## Prep Work:

Note: Transfer supplies into anaerobic chamber at least 24 hours prior to starting work.

### Determine Plate Layout(s)

1. Record layout(s) using [96-Well Plate Template](https://github.com/BisanzLab/Templates/blob/main/multiwell_plates.xlsx)

Details to consider:
  - Plate must contain vehicle controls for each microbe and solvent combination.
  - Plate must contain sterile controls.
  - Ideally, each condition should be preformed with four replicates.
  - This means that plates can typically include 1 strain with 3 drugs, or 1 drug with 3 strains.

### Starter Bacterial Cultures:

Note: Incubation times are variable depending on growth speed of microbe. Allow anywhere between 2-5 days to generate starter culture.

1. Streak desired lab strain onto appropriate solid media in anaerobic chamber. Transfer plate in 37C incubator. 
2. Grow plates for up to 72 hours (Checking for visible colonies)
3. Optional: Follow [Isolate 16S Gene Sequencing Protocol](https://github.com/BisanzLab/LabProtocols/blob/main/Isolate_16S.md) to verify Strain ID.
4. Transfer 1 colony from plate into 5 mL of media in 16 mL glass culture tube. An additional 5 mL tube should be used as a sterile control
5. Culture in 37C incubator overnight or up to 48 hours. (Checking for turbid cultures)

### Drugs

Note: Test solubility of compound prior to starting assay in both desired solvent and after dilution into media.

1. Aliquot drug into 2 mL screw top tubes.
2. Transfer into anaerobic chamber with desired solvent and appropriate syringe filter.

## Day of Experiment:

### Starter Bacterial Cultures:

Note: Traditionally, clinical MIC assays are seeded with 5 x 10e5 bacterial cells and this is determined using McFarland's reagent. Instead, we approximate cell density using OD measurements. 

1. Measure optical density (OD600) of bacterial cultures. 
2. Dilute cultures to 0.1 OD to generate loading inoculum.

### Drugs and Media

Note: Some microbes have altered growth at high solvent concentrations (ex. Above 1-2% DMSO). It can make sense to test a dilution series of vehicle only to check for effects. 

1. Reconstitute drug to final concentration of 51.2 mg/mL (or 200X Highest Concentration) in appropriate solvent.
2. Add 1% reconstitute d drug to sufficient drug media stock (ex. If whole plate, 12 wells * 200 uL = 2400 uL and round to 3 mL. So, add 30 uL of drug stock to 3 mL of media)
3. Add 0.5% vehicle to make sufficient vehicle media stock (This percent vehicle would correspond to the top drug concentration.)
4. Filter sterilize both media stocks.

### Preparation of plate:

Note: Preform all pipetteing steps with multichannel pipetter.

1.	In a 96-well plate, add 100 uL of appropriate media to rows B-F, and H.
2.	Add 200 uL of drug media stock to Row A.
3.	Serially dilute the media containing the drug by pipetting 100 uL and dispensing onto the next row stopping with Row F. (Replace tips between each dilution)
4.  Discard 100 uL from Row F.
5.	Add 100 uL of appropriate media to each well in rows A-F and H to bring final volume to 200 uL.
6.  Add 200 uL of vehicle media stock to Row G.
7.  Transfer 2 uL of loading inoculum appropriate wells of the prepared plate.
8.  Carefully place the cover on the plate and tape around the edges to seal the plate.

An example of concentrations and bacterial conditions:

| Row | Drug | Relative Concentration | Treatment
|-------------|--------------------|--------------------|--------------------|
| A   | 256 ug/mL          | 1X | Bacteria |
| B   | 128 ug/mL          | 0.5X | Bacteria |
| C  | 64 ug/mL          | 0.25X | Bacteria |
| D   | 32 ug/mL          | 0.125X | Bacteria |
| E   | 16 ug/mL          | 0.0625X | Bacteria |
| F   | 8 ug/mL          | 0.03125X | Bacteria |
| G   | 0 ug/mL          | 0 | Bacteria |
| H   | 256 ug/mL          | 1X | Sterile |

### Plate Reader Setup

Note: Select appropriate assay time depending on how fast microbe reaches stationary phase. Faster microbes will be done within 24 hours while others may take up to 48 hours.

1.	Place the plate into the plate reader.
2.	Set up the plate with the following parameters:
    1.	Set incubator temperature to 37C
    2.	Kinetic loop set for XX hours
    3.	Read every 15 minutes
    4.	Shake for 30 sec before reading
4.	When finished, save and export the data.
