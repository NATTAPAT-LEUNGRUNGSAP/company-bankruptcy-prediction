# Company Bankruptcy Prediction

This project explores how financial ratios relate to company bankruptcy and compares two XGBoost models on a held-out test set. The notebook covers exploratory data analysis, company segmentation, and model evaluation.

## Results

| Model | Average precision | Recall at 0.5 | Precision at 0.5 |
|---|---:|---:|---:|
| Baseline XGBoost | 0.504 | 29.5% | 52.0% |
| XGBoost with feature selection, outlier filtering, and SMOTE | 0.403 | 97.7% | 11.1% |

The baseline achieved higher average precision. At a threshold of 0.5, the engineered model detected 43 of the 44 bankrupt companies in the test set, but only about one in nine of its bankruptcy alerts was correct. These figures come from the saved notebook run.

## Run the notebook

From the repository root, install the dependencies and start JupyterLab.

```bash
python -m pip install jupyterlab pandas numpy matplotlib scipy scikit-learn xgboost imbalanced-learn
python -m jupyterlab
```

Open the notebook linked below and run its cells in order. It loads the original CSV and generates figures and a segmented CSV.

## Project files

- [Analysis and modeling notebook](1.%20Source%20Code%20%26%20EDA/nb_company_bankruptcy_predictionR1.ipynb)
- [Original dataset](3.%20Dataset/data_bankruptcy.csv)
- [Segmented dataset](1.%20Source%20Code%20%26%20EDA/data_bankruptcy_segmented.csv)
- [Project report](2.%20Presentation%20%26%20Dashboard/Bankruptcy_Prediction_Report.pdf)
- [Presentation slides](2.%20Presentation%20%26%20Dashboard/Bankruptcy%20Prediction.pdf)
