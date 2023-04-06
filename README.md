# CTS_Test
This repository contains the various routines used to develop the Clinical Trial Selector (CTS). The data loading functions are based on the Synthetic Veteran Suicide Dataset (SVSD). 

The basic workflow for the CTS parser is as follows:
1. Collect .csv files that make up SVSD
2. Extract EHR for a patient
3. Preprocess the EHR using NLP techniques
4. Run NER model on preprocessed data
5. Map entities to medical concepts
6. Generate list of conditions that define the patient based on entities from previous step
7. Query for clinical trials based on conditions from above
8. Preprocess the eligibility criteria for each clinical trial using NLP techniques
9. Run NER model on eligibility criteria for each clinical trial
10. Map the terms in the eligibility criteria to medical concepts
11. Calculate the Sorensen-Dice Index (SDI) between the patient and each clinical trial

The function returns a dataframe containing ALL queried clinical trials. Future versions will return a dataframe with clinical trials that have an SDI  above a predfined threshold value.
