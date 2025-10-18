# LC-MS/MS Bioanalytical Method Protocol

**Protocol:** LC-MS/MS Bioanalytical Method Development  
**Version:** 3.1  
**Date:** August 1, 2025  
**Author:** Dr. Yuki Tanaka  
**Reviewer:** Dr. Elena Popov  
**Approved by:** Dr. Patricia O'Brien

## Overview
This protocol describes the development and validation of LC-MS/MS bioanalytical methods for quantitative analysis of small molecule drugs in biological matrices. This method has been successfully applied to NGT-147 and BTK PROTACs.

## Equipment and Materials

### LC-MS/MS System
- **LC System:** Agilent 1290 Infinity II UPLC
- **MS System:** Agilent 6470 Triple Quadrupole
- **Column:** Waters ACQUITY UPLC BEH C18 (2.1 × 50 mm, 1.7 μm)
- **Autosampler:** Agilent 1290 Infinity II Autosampler
- **Column Oven:** Agilent 1290 Infinity II Column Compartment

### Reagents and Standards
- **Mobile Phase A:** 0.1% Formic acid in water
- **Mobile Phase B:** 0.1% Formic acid in acetonitrile
- **Internal Standard:** Stable isotope-labeled compound
- **Calibration Standards:** 8-point calibration curve (1-1000 ng/mL)
- **Quality Controls:** Low, medium, high QC samples

## Method Development

### 1. Sample Preparation
1. **Plasma Samples:** Thaw at room temperature
2. **Protein Precipitation:** Add 3 volumes of acetonitrile
3. **Centrifugation:** 10,000 × g for 10 minutes
4. **Supernatant:** Transfer to autosampler vials
5. **Injection Volume:** 5 μL

### 2. LC Conditions
- **Flow Rate:** 0.4 mL/min
- **Column Temperature:** 40°C
- **Gradient Program:**
  - 0-0.5 min: 5% B
  - 0.5-2.0 min: 5-95% B
  - 2.0-2.5 min: 95% B
  - 2.5-2.6 min: 95-5% B
  - 2.6-3.0 min: 5% B

### 3. MS Conditions
- **Ionization Mode:** ESI positive
- **Capillary Voltage:** 3500 V
- **Nebulizer Pressure:** 35 psi
- **Drying Gas:** 10 L/min at 300°C
- **Sheath Gas:** 11 L/min at 250°C

### 4. MRM Transitions
- **NGT-147:** 456.5 → 289.1 (quantifier), 456.5 → 245.2 (qualifier)
- **BTK-003:** 678.4 → 445.2 (quantifier), 678.4 → 289.1 (qualifier)
- **Internal Standard:** 459.5 → 292.1

## Method Validation

### 1. Selectivity
- **Matrix Interference:** <20% of LLOQ response
- **Internal Standard:** No interference at retention time
- **Blank Samples:** No peaks at analyte retention times

### 2. Linearity
- **Calibration Range:** 1-1000 ng/mL
- **Correlation Coefficient:** R² > 0.99
- **Back-calculated Concentrations:** Within ±15% of nominal

### 3. Accuracy and Precision
- **Intra-day Accuracy:** 85-115% of nominal
- **Inter-day Accuracy:** 85-115% of nominal
- **Intra-day Precision:** CV < 15%
- **Inter-day Precision:** CV < 15%

### 4. Recovery
- **Extraction Recovery:** >80% for all analytes
- **Matrix Effect:** <20% suppression/enhancement
- **Process Efficiency:** >60%

### 5. Stability
- **Room Temperature:** 24 hours
- **Refrigerated:** 7 days
- **Frozen:** 30 days
- **Freeze-thaw:** 3 cycles
- **Autosampler:** 24 hours

## Quality Control

### Calibration Standards
- **Concentration Range:** 1, 5, 10, 50, 100, 250, 500, 1000 ng/mL
- **Acceptance Criteria:** R² > 0.99, back-calculated within ±15%

### Quality Control Samples
- **LLOQ QC:** 1 ng/mL
- **Low QC:** 3 ng/mL
- **Medium QC:** 300 ng/mL
- **High QC:** 800 ng/mL
- **Acceptance Criteria:** Within ±15% of nominal

### System Suitability
- **Retention Time:** ±2% of expected
- **Peak Shape:** Asymmetry factor 0.8-1.5
- **Signal-to-Noise:** >10 for LLOQ
- **Resolution:** >1.5 between analyte and IS

## Data Analysis

### 1. Calibration Curve
- **Regression:** Linear with 1/x² weighting
- **Acceptance:** R² > 0.99
- **Back-calculation:** Within ±15% of nominal

### 2. Sample Analysis
- **Quantification:** Peak area ratio vs calibration curve
- **Acceptance:** QC samples within ±15% of nominal
- **Reinjection:** If QC fails, reinject calibration curve

### 3. Reporting
- **Concentration:** ng/mL with 3 significant figures
- **Below LLOQ:** Report as <1 ng/mL
- **Above ULOQ:** Dilute and reanalyze

## Troubleshooting

### Common Issues
1. **Poor Peak Shape:** Check column condition and mobile phase
2. **Low Sensitivity:** Optimize MS parameters and sample preparation
3. **Matrix Interference:** Improve sample cleanup or change column
4. **Retention Time Shift:** Check mobile phase composition and column

### Maintenance
- **Column:** Replace every 1000 injections
- **MS Source:** Clean every 500 injections
- **Autosampler:** Clean monthly
- **Calibration:** Daily calibration verification

## Applications

### Current Uses
- **NGT-147:** Plasma and brain tissue analysis
- **BTK PROTACs:** Plasma and cell lysate analysis
- **CDK2 Inhibitors:** Plasma and tumor tissue analysis

### Future Applications
- **Metabolite Identification:** MS/MS fragmentation
- **Protein Binding:** Equilibrium dialysis
- **Tissue Distribution:** Quantitative whole-body autoradiography

## Safety Considerations

- **Chemical Safety:** Handle organic solvents in fume hood
- **Electrical Safety:** Ensure proper grounding
- **Radiation Safety:** Follow MS safety protocols
- **Waste Disposal:** Dispose of organic waste properly

## References
1. FDA Guidance for Industry: Bioanalytical Method Validation (2018)
2. ICH M10: Bioanalytical Method Validation and Study Sample Analysis (2022)
3. Viswanathan et al. (2007) Quantitative bioanalytical methods validation and implementation: Best practices for chromatographic and ligand binding assays. AAPS J.

---

**Protocol Review:** Quarterly  
**Next Review:** November 2025  
**Distribution:** Preclinical Development Team
