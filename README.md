# Human-Centered Data Science Methods for Diabetes Diagnosis 

<!--te-->
About the repository
============
The code provided in this repository belongs to the work completed for the class CDAD-UH 1044Q Human-Centered Data Science at NYU Abu Dhabi. The code is provided for reproducibility and application of the system and training framework to external clinical datasets.

Background
----------
ICUs often lack verified medical histories for incoming patients. Patients who are in distress or brought in confused or unresponsive may not be able to provide information about chronic conditions such as heart disease, injuries, or diabetes. Medical records may take days to transfer, especially for a patient from another medical provider or system. As such, any information that can be provided in a timely manner about chronic conditions such as diabetes can help healthcare workers make better clinical decisions and consequently lead to an improvement in patient outcomes, potentially saving lives.
On top of this, analyses aiming to diagnose chronic conditions typically trade off either model interpretability or accuracy. This analysis attempts to fill both these gaps by training LGBM and CatBoost classifiers on data from MIT's GOSSIS (Global Open Source Severity of Illness Score) Initiative and subsequently interpreting the predictions made by these models to reduce the need for a trade-off between model interpretability and accuracy. 

Overview
--------
The proposed system predicts the probability of an ICU patient having diabetes mellitus and interprets these predictions. 

Requirements
--------------
This project requires the following libraries and frameworks as well as Python3:

- `numpy`
- `pandas`
- `matplotlib`
- `sklearn`
- `pycaret`
- `lightgbm`
- `catboost`
- `shap`

Repository Content
====================


dataset
--------
The dataset folder includes a data file, which is later split into train and test sets (80-20 split). This test set is provided to demonstrate how the trained models are applied to real ICU data.
This data was taken from the [Women in Data Science (WiDS) Datathon 2021](https://www.kaggle.com/c/widsdatathon2021/overview/description).

code
-----------------------------

This folder includes the scripts used to preprocess and clean the raw data, compare a set of commonly used classifiers, feature select, tune and train models, implement ensemble learning, and generate interpretability for model outputs.
To reproduce the results of this analysis, uncomment code cell 12 in _cleaning-testing-fs.ipynb_ and run all cells in the notebook, then run all cells in _tuning-ensembling-results.ipynb_.
