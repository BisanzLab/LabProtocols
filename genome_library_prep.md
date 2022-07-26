# KAPA EvoPlus Kit

## Notes

This protocol is derived from the KAPA EvoPlus instruction manuals scaling reaction volumes by a 5-fold factor to facilitate increased throughput.

## Materials 
- [ ] KAPA UDI Adapter Kit 15uM (Roche 8861919702)
- [ ] KAPA HyperPure Beads Kit (Roche 8963835001)
- [ ] 10 mM Tris-HCl, pH 8.0
- [ ] 80% ethanol
- [ ] nuclease free water
- [ ] Thermocycler
- [ ] Magnetic stand
- [ ] 0.2 mL tube or PCR plate
- [ ] Spead vac

## Procedure

### Prepare the Sample Library

#### Step 0: Sample Preparation
1. Using quantificaiton derived from the Qubit, dilute gDNA to 10 ng/µl with a minimum volume of 7µL in 10 mM Tris-HCl.
*Safe stopping point, store at -20˚C*

#### Step 1: Fragmentation and A-Tailing
1. Transfer gDNA into strip tube or 96 well plate.
2. Vortex the FragTail ReadyMix well and centrifuge briefly. 
3. Assemble each Fragmentation and A-tailing reaction on ice as follows:

|Component|Volume Per Individual Sample|
|---------|:---:|
|70 ng DNA  |7 μL                                          
|FragTail ReadyMix  |5 μL                     
|**Total**    |**12 μL**                     
                    
4. Mix each Fragmentation and A-tailing reaction thoroughly and centrifuge briefly. Return the plate/tube(s) on ice and proceed immediately to the next step. 
5. Incubate in a thermocycler, pre-cooled to +4°C  and programmed as outlined below. Set the lid temperature to ~ +65°C .
	a. Pre-cool block: +4°C
	b. Fragmentation: +37°C - See table below
	c. A-tailing: +55°C for 30 minutes
	d. Hold: +4°C

|Estimated Fragment Length|Fragmentation Time at 37°C  |
|:---:|:---:|
|550-640 bp|5 min                                           
|330-410 bp|10 min                   
|240-320 bp|15 min                    
|200-260 bp|20 min                      
|170-230 bp|25 min
|140-210 bp|30 min                   

#### Step 2: Adapter Ligation

1. Transfer the reaction on ice and proceed to Adapter Ligation.
2. Vortex the Ligation ReadyMix well and centrifuge briefly and the following in the specified order:
	a. Add 1 µL of a unique KAPA UDI Adapter to each tube/well containing sample from the previous step.
	b. Add 2 µL of the Ligation ReadyMix to each tube/well containing 12 µL sample and 1 µL KAPA UDI Adapter, resulting in a total volume of 15 µL.

|Component|Volume Per Individual Sample |
|----------|:---:|
|FragTail Product|12 μL                                         
|KAPA UDI Adapter|1 μL                 
|Ligation|2 μL                   
|**Total**|15 μL                     

	c. Mix the ligation reaction thoroughly and centrifuge.
	d. Incubate the ligation reaction at +20°C on a thermocycler for 15 minutes.
	e. Following the incubation, proceed immediately to the next step.
  
#### Step 3: Purify the Sample Library using KAPA HyperPure Beads

1. To each ligation reaction, add 12 μL of room temperature KAPA HyperPure Beads that have
been thoroughly resuspended.

|Component|Volume Per Individual Sample |
|----------|:---:|
|Ligation Reaction Product|15 μL                                         
|KAPA HyperPure Beads|12 μL                                 
|**Total**|27 μL

2. Once added, mix thoroughly and centrifuge briefly.
3. Incubate the sample at room temperature for 5 minutes to allow the sample library to bind to the beads.
4. Place the sample on a magnet to capture the beads. Incubate until the liquid is clear.
5. Carefully remove and discard the supernatant.
6. Keeping the sample on the magnet, add 40 μL of freshly-prepared 80% ethanol.
7. Incubate the sample at room temperature for ≥30 seconds.
8. Carefully remove and discard the ethanol.
9. Keeping the sample on the magnet, add 40 μL of freshly-prepared 80% ethanol.
10. Incubate the sample at room temperature for ≥30 seconds.
11. Carefully remove and discard the ethanol. Remove residual ethanol without disturbing the
beads.
12. Allow the beads to dry at room temperature, sufficiently for all the ethanol to evaporate.
13. Remove the sample from the magnet.
14. Thoroughly resuspend the beads in 25 µL (or appropriate volume) of nuclease free water. 
15. Incubate the sample at room temperature for 2 minutes to allow the sample library to elute off the beads.
16. Place the sample on the magnet to collect the beads. Incubate until the liquid is clear.
17. Transfer an appropriate volume of the eluate to a fresh tube/well.
18. Move samples to a appropriate speed vac and dry to completion.
19. Resuspend in 4 µL 10mM Tris-HCl.
20. Proceed immediately to amplify the sample library.

### Amplify the Sample Library

#### Step 1: Prepare the Library Amplification Reaction
1. Assemble each library amplification reaction as follows:

|Component|Volume Per Individual Library |
|:---|:---:|
|2X HiFi Hotstart ReadyMix|5 μL                                         
|10X Illumina Library Amplification Primer Mix|1 μL   
|Adapter-ligated Library| 4 μL                                
|**Total**|10 μL

2. Mix thoroughly and centrifuge briefly. Immediately proceed to the next step. 


##### Step 2: Perform the library Amplification

1. Place the sample in the thermocycler and amplify the adapter-ligated library using the following Library
Amplification program with the lid temperature set to +105°C:
	a. Step 1: 45 seconds at +98°C
	b. Step 2: 15 seconds at +98°C
	c. Step 3: 30 seconds at +60°C
	d. Step 4: 30 seconds at +72°C
	e. Step 5: Go to Step 2, repeat 4x
	f. Step 6: 1 minute at +72°C
	g. Step 7: Hold at +4°C

|Input Amount|Number of Amplification Cycles for WGS to achieve 4 nM |
|:---:|:---:|
|500 ng|0 (PCR-free)                                        
|250 ng|0 (PCR-free)
|100 ng|0 (PCR-free)    
|75 ng |0 (PCR-free)
|50 ng |1-2 cycles
|10 ng |5-7 cycles                          

### Purify the Amplified Sample Library using KAPA HyperPure Beads**

1. Add 10 μL of room temperature, thoroughly resuspended, KAPA HyperPure Beads to each amplified sample
library.
2. Mix the amplified sample library and KAPA HyperPure Beads thoroughly and centrifuge briefly.
3. Incubate the sample at room temperature for 5 minutes to allow the sample library to bind to the beads.
4. Place the sample on a magnet to capture the beads. Incubate until the liquid is clear.
5. Carefully remove and discard the supernatant.
6. Keeping the sample on the magnet, add 40 μL of freshly-prepared 80% ethanol.
7. Incubate the sample at room temperature for ≥30 seconds.
8. Carefully remove and discard the ethanol.
9. Keeping the sample on the magnet, add 40 μL of freshly-prepared 80% ethanol.
10. Incubate the sample at room temperature for ≥30 seconds.
11. Carefully remove and discard the ethanol. Remove residual ethanol without disturbing the beads.
12. Allow the beads to dry at room temperature, sufficiently for all of the ethanol to evaporate.
13. Remove the sample from the magnet.
14. Thoroughly resuspend the beads in 25 μL (or appropriate volume) of 10 mM Tris-HCl, pH 8.0.
15. Incubate the sample at room temperature for 2 minutes to allow the sample library to elute off the beads.
16. Place the sample on the magnet to capture the beads. Incubate until the liquid is clear.
17. Transfer 20 μL of the eluate to a new tube/well.
18. Purified, amplified sample libraries can be stored at +2 to +8°C for 1 - 2 weeks or at -15 to -25°C for up to 3 months. 

### Pooling

WIP
