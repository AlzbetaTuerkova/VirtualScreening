# VirtualScreening
The repository contains supplementary files to our study where a consensus screening approach by using different types of machine learning models (proteochemometric models, conformal prediction models, and QSAR models), followed by structure-based virtual screening of preselected hits using the structural models for hepatic OATPs was performed.

### Models_XGBoost
This contains the XGBoost models used in XML format created with Pipeline Pilot 18.1.100.
The QSAR_All model was formed by combining the three individual QSAR models, while the PCM model was made once and applied to the individual models due to the nature of PCM. Detailed information can be found in the article.

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

### 44_compound_IC50.xls
This .xls file contains IC50 measurements from the first round of in vitro screening (n=44 compounds). Compound InChiKey, ZINC ID, canonical smiles, IC50 values, and average number of measurements, are listed in the .xls table.

### 6_compounds_poses.zip
This .zip file contains docking data (.pdb files for the transporter and calculated poses) for the six compounds identified on the basis of the full dose curve measurements. 

### G1.csv
This .csv file contains a list of 15 pre-selected OATP1B1 hits for experimental testing. Compound InChiKey, group label (based on the machine learning model used), and scoring function from the compound docking into OATP1B1, OATP1B3, and OATP2B1, respectively, is listed in the .csv table. 

### G2.csv
This .csv file contains a list of 15 pre-selected OATP1B3 hits for experimental testing. Compound InChiKey, group label (based on the machine learning model used), and scoring function from the compound docking into OATP1B1, OATP1B3, and OATP2B1, respectively, is listed in the .csv table. 

### G3.csv
This .csv file contains a list of 15 pre-selected OATP2B1 hits for experimental testing. Compound InChiKey, group label (based on the machine learning model used), and scoring function from the compound docking into OATP1B1, OATP1B3, and OATP2B1, respectively, is listed in the .csv table. 

### Models_Conformal_Prediction.zip
This .zip file contains conformal prediction models for OATP1B1, OATP1B3, and OATP2B1 transporters.

### OATP1B1_actives.zip
This .zip file contains conformal docking poses for all OATP1B1 actives identified in the fist round of experimental testing. 

### OATP1B3_actives.zip
This .zip file contains conformal docking poses for all OATP1B3 actives identified in the fist round of experimental testing. 

### OATP1B1_actives.zip
This .zip file contains conformal docking poses for all OATP2B1 actives identified in the fist round of experimental testing. 





