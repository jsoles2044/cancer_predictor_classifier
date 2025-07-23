# AWS AutoGluon Machine Learning Classification Project

This project demonstrates how to train a classification model using [AutoGluon](https://auto.gluon.ai/stable/index.html), 
an open-source AutoML toolkit developed by AWS. It includes data loading, visualization, and model training using tabular data.

## 🛠️ Requirements

- Python 3.8 – 3.10
- AutoGluon
- pandas
- numpy
- matplotlib
- seaborn
- jupyterthemes

## 📦 Installation

```bash
pip install autogluon.tabular pandas numpy matplotlib seaborn jupyterthemes
```

If running in Google Colab:

```bash
!pip install -U ipykernel
```

## 🚀 Usage

1. Set notebook styling for better readability:

```python
from jupyterthemes import jtplot
jtplot.style(theme='monokai', context='notebook', ticks=True, grid=False)
```

2. Import dependencies:

```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```

3. Train a model with AutoGluon:

```python
from autogluon.tabular import TabularDataset, TabularPredictor

train_data = TabularDataset('your_data.csv')
predictor = TabularPredictor(label='target_column').fit(train_data)
```

4. Evaluate:

```python
predictor.leaderboard(test_data, silent=True)
```

## 📌 Notes

- If plot labels appear dark or unreadable, use `jtplot.style()` to apply a better theme.
- Adjust `time_limit` and `presets` in `.fit()` to balance training time and performance.

---

