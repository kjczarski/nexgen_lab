# NanoBRET Target Engagement Assay Protocol

**Assay:** NanoBRET Target Engagement  
**Version:** 1.3  
**Date:** June 10, 2025  
**Author:** Dr. Kevin Zhao  
**Reviewer:** Dr. Rachel Foster  
**Approved by:** Dr. Michael Torres

## Overview
This protocol describes the NanoBRET target engagement assay for measuring compound binding to target proteins in live cells. Used extensively for EGFR and BTK programs.

## Principle
NanoBRET (NanoLuc Binary Technology) uses energy transfer between NanoLuc luciferase and HaloTag fluorescent protein to measure protein-protein interactions and target engagement.

## Materials

### Reagents
- **NanoLuc Substrate:** Nano-Glo Live Cell Reagent (Promega)
- **HaloTag Ligand:** HaloTag TMR Ligand (Promega)
- **Cell Culture Medium:** RPMI-1640 + 10% FBS
- **Assay Buffer:** HEPES-buffered saline
- **Test Compounds:** DMSO stock solutions

### Equipment
- **Plate Reader:** Tecan Spark 20M
- **Incubator:** 37°C, 5% CO2
- **Microplates:** 384-well white plates
- **Pipettes:** Multichannel pipettes

### Cell Lines
- **EGFR:** A549 cells expressing EGFR-NanoLuc
- **BTK:** Ramos cells expressing BTK-NanoLuc
- **Control:** Parental cells (no fusion protein)

## Procedure

### 1. Cell Preparation
1. **Culture:** Maintain cells in complete medium
2. **Passage:** Split 1:10 every 3-4 days
3. **Seeding:** 10,000 cells/well in 384-well plates
4. **Incubation:** 24 hours at 37°C, 5% CO2

### 2. Compound Treatment
1. **Dilution:** Prepare compound dilutions in assay buffer
2. **Addition:** Add 10μL compound solution per well
3. **Incubation:** 30 minutes at 37°C
4. **Controls:** DMSO (0.1%) and reference compound

### 3. Substrate Addition
1. **NanoLuc Substrate:** Add 10μL Nano-Glo reagent
2. **HaloTag Ligand:** Add 1μL TMR ligand (1μM final)
3. **Incubation:** 10 minutes at room temperature
4. **Reading:** Measure luminescence and fluorescence

### 4. Data Collection
- **Luminescence:** 450nm (NanoLuc signal)
- **Fluorescence:** 585nm (TMR signal)
- **BRET Ratio:** Fluorescence/Luminescence
- **Target Engagement:** % inhibition of BRET signal

## Data Analysis

### Calculations
- **BRET Ratio:** TMR signal / NanoLuc signal
- **% Inhibition:** (1 - BRET_compound/BRET_DMSO) × 100
- **IC50:** Curve fitting using GraphPad Prism
- **Statistical Analysis:** n=3, mean ± SEM

### Quality Control
- **Z' Factor:** >0.5 (acceptable)
- **CV:** <15% (intra-assay)
- **Reference Compound:** Gefitinib (EGFR), Ibrutinib (BTK)

## Example Results

### EGFR Target Engagement (NGT-147)
- **IC50:** 2.5 nM
- **Max Inhibition:** 95%
- **Hill Slope:** 1.2
- **R²:** 0.98

### BTK Target Engagement (BTK-003)
- **IC50:** 15 nM
- **Max Inhibition:** 88%
- **Hill Slope:** 1.1
- **R²:** 0.96

## Troubleshooting

### Common Issues
1. **Low Signal:** Check cell density, substrate concentration
2. **High Background:** Optimize HaloTag ligand concentration
3. **Poor Reproducibility:** Ensure consistent cell passage number
4. **Compound Interference:** Check DMSO concentration

### Optimization Tips
- **Cell Density:** 8,000-12,000 cells/well optimal
- **Incubation Time:** 30 minutes for most compounds
- **Substrate Ratio:** 1:1 NanoLuc:TMR for best signal
- **Temperature:** Room temperature for reading

## Applications

### Current Uses
- **EGFR Program:** NGT-147 target engagement
- **BTK Program:** BTK-003 PROTAC binding
- **CDK2 Program:** Hit validation
- **Project Aurora:** Novel target validation

### Future Applications
- **Kinase Profiling:** Selectivity assessment
- **Mechanism Studies:** Binding kinetics
- **Screening:** High-throughput target engagement

## Safety Considerations

- **Biosafety Level:** BSL-2
- **Waste Disposal:** Biohazard containers
- **Personal Protection:** Lab coat, gloves
- **Decontamination:** 10% bleach solution

## References
1. Machleidt et al. (2015) NanoBRET - A Novel BRET Platform for the Analysis of Protein-Protein Interactions. ACS Chem Biol.
2. Robers et al. (2015) Target engagement and drug residence time can be observed in living cells with BRET. Nat Commun.

---

**Protocol Review:** Quarterly  
**Next Review:** September 2025  
**Distribution:** Biology Team, Screening Team

