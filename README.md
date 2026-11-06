# PETRA-Notebook-14-SHAP

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mansoorz353/PETRA-Notebook-14-SHAP/blob/main/Notebook_14_4_SHAP_Diagnosis.ipynb)

This repository contains the code and data supporting **Chapter 14** workflows, focusing on SHAP-based model diagnosis for well performance analysis.

## Getting Started

You can run this notebook directly in your browser using Google Colab by clicking the badge above. 

To ensure the dataset and model load correctly when executing the notebook in Colab, include the following snippet at the top of your code:

```python
import pandas as pd
import pickle
import os

# Download files from GitHub if running in Google Colab
if 'google.colab' in str(get_ipython()):
    !wget -nc [https://raw.githubusercontent.com/mansoorz353/PETRA-Notebook-14-SHAP/main/well_diagnosis_dataset.csv](https://raw.githubusercontent.com/mansoorz353/PETRA-Notebook-14-SHAP/main/well_diagnosis_dataset.csv)
    !wget -nc [https://raw.githubusercontent.com/mansoorz353/PETRA-Notebook-14-SHAP/main/xgb_well_diagnosis.pkl](https://raw.githubusercontent.com/mansoorz353/PETRA-Notebook-14-SHAP/main/xgb_well_diagnosis.pkl)

# Load assets
df = pd.read_csv("well_diagnosis_dataset.csv")
with open("xgb_well_diagnosis.pkl", "rb") as f:
    model = pickle.load(f)
