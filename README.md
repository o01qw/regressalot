![Sir Regresssalot](assets/regressaloticon.jpg)
# Regressalot

**Regressalot** is a lightweight AutoML utility designed for **preliminary analysis and model comparison**.  
It helps you quickly assess the performance of multiple machine learning models using default settings and diagnostics — ideal for early exploration before fine-tuning or scaling.

## Features
- One-line run of Linear Regression, Decision Tree, Random Forest, and XGBoost
- Automatic feature encoding
- Evaluation metrics like R², RMSE, RMSPE, over/under-predictions, overfitting
- Ranking of models by performance
- Prediction plots

## Installation
```bash
pip install regressalot
```

## Usage

To run the AutoML pipeline on your regression dataset:
```python
from regressalot import AutoMLRunner

runner = AutoMLRunner(
    data='regression_sample.csv',  # path to your CSV file
    target='target',              # name of the target column
    task='regression'            # task type
)

runner.run()
```

Make sure your dataset has a mix of numerical and/or categorical features and a clearly defined target column. The library automatically encodes categorical features.
