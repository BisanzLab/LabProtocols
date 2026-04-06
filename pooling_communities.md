# Synthetic Bacterial Community Pooling Protocol

---

## 1. Streaking the Strains

1. After strain selection, streak each strain from the glycerol stock.

   * Use printed labels with **strain ID** and **date of streaking**.
2. Use the **three or four-quadrant technique** when streaking.
3. Follow this progression:

   * glycerol stock → plate
   * plate → plate
   * plate → liquid culture
4. **Do not** revive bacteria directly from glycerol stock to liquid culture to prevent contamination.

---

## 2. Strain Verification by Sanger Sequencing

### Instagene DNA Extraction

1. Pipette **100 µL Instagene mix** into each sterile microcentrifuge tube (mix well before pipetting).
2. Transfer a **single colony** of each strain into the tube in an anaerobic chamber.
3. Vortex to mix.
4. Incubate at **56°C for 30 min**, vortex after incubation.
5. Incubate at **100°C for 30 min**, vortex after incubation.
6. Centrifuge at **16,000 × g for 3 min**.
7. Transfer **60 µL supernatant** to a new tube (optional; can use directly for PCR).
8. Store gDNA at:

   * **−20°C** for long-term
   * **4°C** for short-term

Reference protocol: [BisanzLab Isolate 16S Protocol](https://github.com/BisanzLab/LabProtocols/blob/main/Isolate_16S.md)

---

### PCR Amplification

**Master mix (per 20 µL reaction):**

| Component        | Stock Conc. | Final Conc. | Volume (µL) |
| ---------------- | ----------- | ----------- | ----------- |
| Amplitaq Gold 2× | 2×          | 1×          | 10          |
| 8F primer        | 2 µM        | 400 nM      | 4           |
| 1542R primer     | 2 µM        | 400 nM      | 4           |
| gDNA             | variable    | variable    | 2           |
| **Total**        | -           | -           | **20**      |

* Include a **no-template control (NTC)** using 2 µL water.
* Pop spin to remove air bubbles.

**PCR cycle parameters:**

| Step                  | Temperature (°C) | Time   |
| --------------------- | ---------------- | ------ |
| Initial denaturation  | 95               | 10 min |
| Denature (×30 cycles) | 95               | 30 sec |
| Anneal                | 55               | 30 sec |
| Extend                | 72               | 60 sec |
| Final hold            | 4                | Hold   |

---

### PCR Clean-Up (AMPure XP Beads)

1. Add **36 µL AMPure XP beads** (1.8× volume) to each **20 µL PCR reaction**.
2. Mix by pipetting, incubate **5 min** on magnetic rack.
3. Keep tubes on rack:

   * Remove supernatant
   * Add **200 µL fresh 70% ethanol**, repeat twice
   * Remove supernatant completely
4. Pop spin to collect remaining ethanol and remove it.
5. Air dry beads for **~10 min**.
6. Add **25 µL nuclease-free water**, mix, incubate **2–5 min** on rack.
7. Transfer **20 µL eluted DNA** to a fresh tube, discard beads.

---

### Sanger Sequencing

1. Send purified PCR products to **Genewiz**.
2. Open `.ab1` files in **4Peaks** (or equivalent).
3. Trim low-quality regions at the start and end.
4. Check sequence accuracy manually.

Example image:
![4peaks](https://github.com/SusanTian/images/blob/main/Screenshot%202025-11-03%20at%2012.26.55.png)

**FASTA file formatting example:**

```
>strain1
ATTTCCGGGGGG...
>strain2
ATTCCGGAATAT...
```

Save as `sanger_input.fa`.

---

## 3. BLAST Verification

Use BLAST to compare Sanger sequences against the lab strain database or other reference database.

**Example command:**

```bash
conda activate blast_2.12.0

blastn \
  -query path_to_sanger_input.fa \
  -db path_to_database \
  -out path_to_output/Sanger_16S_blast.txt \
  -num_threads 18 \
  -outfmt "6 qseqid sseqid sstrand qlen slen nident pident qstart qend sstart send length mismatch evalue"
```

---

## 4. Post-BLAST Analysis in R

```r
library(tidyverse)

read_tsv("/path_to_output/Sanger_16S_blast.txt",
  col_names = c("FeatureID", "Subject", "Strand", "Query_Length", "Subject_Length",
                "N_identities", "Percent_Identity", "Query_Start", "Query_end",
                "Subject_Start", "Subject_End", "Alignment_Length", "NMismatch", "evalue")) %>%
  mutate(Coverage = Alignment_Length / if_else(Query_Length < Subject_Length, Query_Length, Subject_Length) * 100) %>%
  filter(Percent_Identity >= 97) %>%
  interactive_table()
```

---

## 5. Manual Verification

* Confirm that each strain matches the expected species.
* For uncertain matches, re-check sequences using the **NCBI BLAST web interface** against the 16S database.

---

## 6. Sanger Verification Using isolateR

```r
library(isolateR)
library(sangerseqR)
library(sangeranalyseR)

filepath1 <- "~/path_to_folders_with_ab1_files/"

isoQC.S4 <- isoQC(
  input = filepath1,
  export_html = TRUE,
  export_csv = TRUE,
  export_fasta = TRUE,
  verbose = TRUE,
  min_phred_score = 20,
  min_length = 200,
  sliding_window_cutoff = NULL,
  sliding_window_size = 15
)

isoTAX.S4 <- isoTAX(
  input = "/absolute/path_to_folders_with_ab1_files/isolateR_output/01_isoQC_trimmed_sequences_PASS.csv",
  export_html = TRUE,
  export_csv = TRUE,
  db = "16S",
  quick_search = TRUE,
  phylum_threshold = 75.0,
  class_threshold = 78.5,
  order_threshold = 82.0,
  family_threshold = 86.5,
  genus_threshold = 96.5,
  species_threshold = 98.7
)

setwd("~/path_to_folders_with_ab1_files")
```

---

## 7. Pooling the Strains

Two pooling methods:

* **Liquid culture method**: slower, better for tiny colonies, includes washing step.
* **Agar plate method**: faster, may not work for very small colonies, no washing step needed.

---

### Method 1: Liquid Culture

1. Set up a liquid culture of each strain using sterile technique.

   * It is recommended to start slow-growing strains first and fast-growing strains later so that the latter remain fresh and viable on the day of pooling.
2. Once all cultures are ready:

   * Vortex each culture tube to mix thoroughly.
   * Measure OD600, including blanks for background subtraction. Adjust OD values accordingly.
3. Calculate the pooling volume of each culture to reach the desired final OD.

   * Example: If the adjusted OD of strain `JEB00015` is 0.8 and the target pooled OD600 is 80, use **100 µL** of the `JEB00015` culture.
4. Transfer the calculated volume of each culture into microcentrifuge tubes. Spin to pellet the cells, then remove the supernatant.
5. Resuspend each pellet in **1 mL BHICHV + 15% glycerol** and combine all resuspended cells.
6. Aliquot the pooled community as needed and store at **–80 °C** for long-term preservation.
7. Sequence one aliquot to assess the **evenness of pooling**.

---

### Method 2: From Agar Plates

1. After verifying strain identity and checking for contamination, scrape a sufficient amount of colonies from each agar plate into microcentrifuge tubes.
2. Resuspend the cells in **BHICHV + 15% glycerol**.
3. Measure OD600, include blanks for background subtraction, and adjust accordingly.
4. Calculate pooling volumes as in the liquid method.

   * Example: If the adjusted OD of strain `JEB00015` is 0.8 and the target pooled OD600 is 80, use **100 µL** of the `JEB00015` suspension.
5. Transfer the correct volumes of each suspension into a conical tube to combine them.
6. Aliquot the pooled community as needed and preserve at **–80 °C** for long-term storage.
7. Sequence one aliquot to verify the **evenness of pooling**.

---
