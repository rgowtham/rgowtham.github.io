+++
title = "Sample First Post"
author = ["Gowtham A R"]
date = 2026-02-22T00:00:00-08:00
draft = false
+++

## Introduction {#introduction}

This is my very first blog post using Hugo + Emacs. I am going to write a code block that pulls in iris dataset and plots the correlation plot between its features.


## Pulling data and plotting {#pulling-data-and-plotting}

```python
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris
import pandas as pd

# Load dataset
iris = load_iris(as_frame=True)
df = iris.frame

# Calculate correlation matrix
corr = df.corr()

# Plot heatmap
plt.figure(figsize=(8, 6))
sns.heatmap(corr, annot=True, cmap='coolwarm', vmin=-1, vmax=1)
plt.title("Iris Dataset Correlation Matrix")
plt.show()
```

{{< figure src="/images/iris_feature_correlation.png" >}}
