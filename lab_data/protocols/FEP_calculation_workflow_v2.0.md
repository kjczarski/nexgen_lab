# FEP Calculation Workflow Protocol

**Protocol:** Free Energy Perturbation (FEP) Calculations  
**Version:** 2.0  
**Date:** March 1, 2025  
**Author:** Dr. Linda Wu  
**Reviewer:** Dr. Amit Patel  
**Approved by:** Dr. Rebecca Chao

## Overview
This protocol describes the Free Energy Perturbation (FEP) calculation workflow used for predicting relative binding free energies of compounds to target proteins. This method has been instrumental in the discovery of NGT-147.

## Software Requirements

### Primary Software
- **Schrödinger Suite:** FEP+ module
- **AMBER:** AMBER20 for MD simulations
- **Python:** Custom analysis scripts
- **Cloud Computing:** AWS EC2 instances

### Hardware Requirements
- **CPU:** 32+ cores per calculation
- **Memory:** 128+ GB RAM
- **Storage:** 1+ TB SSD storage
- **GPU:** Optional for acceleration

## Workflow Steps

### 1. Protein Preparation
1. **Structure Source:** X-ray crystal structure or homology model
2. **Protein Preparation:** Remove water, add hydrogens, optimize H-bonds
3. **Binding Site:** Define binding site (5Å around ligand)
4. **System Setup:** Add explicit solvent (TIP3P water model)

### 2. Ligand Preparation
1. **3D Structure:** Generate 3D conformations
2. **Tautomerization:** Consider all possible tautomers
3. **Protonation:** Determine protonation state at pH 7.4
4. **Charges:** Assign AM1-BCC charges

### 3. FEP+ Setup
1. **Transformation:** Define chemical transformation between compounds
2. **Mapping:** Map atoms between compounds
3. **Lambdas:** Define lambda windows (typically 12 windows)
4. **Constraints:** Apply distance/angle constraints

### 4. Simulation Parameters
- **Temperature:** 300 K
- **Pressure:** 1 atm (NPT ensemble)
- **Timestep:** 2 fs
- **Cutoff:** 9 Å for non-bonded interactions
- **Equilibration:** 1 ns per window
- **Production:** 5 ns per window

### 5. Data Analysis
1. **Free Energy:** Calculate ΔG using BAR method
2. **Error Analysis:** Estimate statistical errors
3. **Convergence:** Check convergence of free energy
4. **Validation:** Compare with experimental data

## Example: NGT-147 Discovery

### Transformation Series
- **NGT-140 → NGT-141:** Addition of fluorine
- **NGT-141 → NGT-142:** Methoxy group modification
- **NGT-142 → NGT-143:** Linker optimization
- **NGT-143 → NGT-147:** Final optimization

### Results
- **Predicted ΔG:** -2.3 kcal/mol (NGT-147 vs NGT-140)
- **Experimental ΔG:** -2.1 kcal/mol
- **Error:** 0.2 kcal/mol (excellent agreement)

## Quality Control

### Validation Criteria
- **Statistical Error:** <0.5 kcal/mol
- **Convergence:** Free energy plateau reached
- **Experimental Agreement:** Within 1 kcal/mol
- **Reproducibility:** Multiple independent runs

### Troubleshooting
1. **Poor Convergence:** Increase simulation time
2. **Large Errors:** Check lambda spacing
3. **Bad Mapping:** Redefine atom mapping
4. **System Issues:** Verify protein preparation

## Applications

### Current Uses
- **EGFR Program:** NGT-147 optimization
- **BTK Program:** PROTAC linker optimization
- **CDK2 Program:** Hit-to-lead optimization
- **Project Aurora:** Novel target validation

### Future Applications
- **Selectivity Prediction:** Off-target binding
- **ADMET Properties:** Solubility, permeability
- **Resistance Mutations:** Drug resistance mechanisms

## Performance Metrics

### Computational Efficiency
- **Time per transformation:** 24-48 hours
- **Cost per calculation:** $200-400 (AWS)
- **Success rate:** 85% (valid predictions)

### Accuracy
- **Mean absolute error:** 0.8 kcal/mol
- **R² correlation:** 0.92
- **Experimental agreement:** 78%

## Safety Considerations

- **Data Security:** Encrypt sensitive data
- **Cloud Usage:** Monitor costs and usage
- **Backup:** Regular data backups
- **Access Control:** Limit access to authorized users

## References
1. Wang et al. (2015) Accurate and reliable prediction of relative ligand binding potency in prospective drug discovery by way of a modern free-energy calculation protocol and force field. J Am Chem Soc.
2. Boresch et al. (2003) Absolute binding free energies: a quantitative approach for their calculation. J Phys Chem B.

---

**Protocol Review:** Quarterly  
**Next Review:** June 2025  
**Distribution:** Computational Chemistry Team
