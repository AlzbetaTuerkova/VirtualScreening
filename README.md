# VirtualScreening
The repository contains supplementary files to our study where a consensus screening approach by using different types of machine learning models (proteochemometric models, conformal prediction models, and QSAR models), followed by structure-based virtual screening of preselected hits using the structural models for hepatic OATPs was performed.

### Models_XGBoost
This contains the used XGBoost models used in XML format created with Pipeline Pilot 18.1.100.

Models were defined as XGBoost models with: (No. means Number of):
- **Molecular Descriptors**:
	- FCFP6
	- ALogP
	- Molecular Weight
	- Hydrogen Donors (No.)
	- Hydrogen Acceptors (No.)
	- Rotatable Bonds (No.)
	- Atoms (No.)
	- Rings (No.)
	- Aromatic Rings (No.)
	- Fragments (No.)
	- NPlusO_count
	- Solubility
	- Surface Area
	- Polar Surface Area
	- Polar SASA
- **XGBoost Options:**
	- Max Trees = 100
	- Learning Rate = 0.3
	- Max Depth = 7
	- Data Fraction = 1.0
	- Descriptor Fraction = 0.7
	- Weighting Method = By Class
	- Booster = gbtree
	- Dropout Fraction 0.2
- **Protein Descriptors** were based on Z-Scales, taking the first three Z-Scales of each protein as described in Hellberg S, Sjöström M, Skagerberg B, Wold S. Peptide quantitative structure-activity relationships, a multivariate approach. J Med Chem. 1987 Jul;30(7):1126–35.

### Model_Input_Output
This folder contains:
- **training_Set_OATP1B1_1B3_2B1.csv** -- the original training set containing OATP1B1, OATP1B3 and OATP2B1 activity values for a variety of tested compounds,
- **combined_list_of_top250_used_for_docking.csv** -- The final set of compounds that were carried over to the 3D phase.

