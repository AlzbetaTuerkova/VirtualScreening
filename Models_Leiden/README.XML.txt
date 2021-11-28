Contains the models used on the Leiden side. Created with Pipeline Pilot 18.1.100.

Models were defined as XGBoost models with: (No. means Number of:
- Molecular Descriptors:
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
- XGBoost Options
	- Max Trees = 100
	- Learning Rate = 0.3
	- Max Depth = 7
	- Data Fraction = 1.0
	- Descriptor Fraction = 0.7
	- Weighting Method = By Class
	- Booster = gbtree
	- Dropout Fraction 0.2
- Protein Descriptors were based on Z-Scales, taking the first three Z-Scales of each protein as described in Hellberg S, Sjöström M, Skagerberg B, Wold S. Peptide quantitative structure-activity relationships, a multivariate approach. J Med Chem. 1987 Jul;30(7):1126–35.