# Statistical Outlier Detection in Python

A structured Python implementation comparing standard statistical techniques to identify anomalies and outliers in numerical datasets.

---

## Detection Techniques

### 1. Interquartile Range (IQR) Method
Identifies outliers based on quartile spread and fence thresholds:
* **$Q_1$ (25th Percentile):** `12.0`
* **$Q_3$ (75th Percentile):** `15.0`
* **$\text{IQR} = Q_3 - Q_1$:** `3.0`
* **Lower Fence ($Q_1 - 1.5 \times \text{IQR}$):** `7.5`
* **Upper Fence ($Q_3 + 1.5 \times \text{IQR}$):** `19.5`
* **Identified Outliers:** `[102, 107, 108]`

### 2. Z-Score Method
Standardizes data using mean ($\mu$) and standard deviation ($\sigma$), flagging points beyond 3 standard deviations ($\vert{}Z\vert{} > 3$):
* **Formula:** $Z = \frac{x - \mu}{\sigma}$
* **Threshold:** $3$
* **Identified Outliers:** `[102, 107, 108]`

### 3. Visual Inspection
* Box plot generated using `seaborn.boxplot()` to visualize median, quartiles, and points falling outside the whiskers.

---

## Tech Stack
* **Python 3**
* **NumPy** (Percentiles, mean, std)
* **Matplotlib & Seaborn** (Data visualization)

---

## Usage

```python
import numpy as np

dataset = [
    11, 10, 12, 14, 12, 15, 14, 13, 15, 102,
    12, 14, 17, 19, 107, 10, 13, 12, 14, 12,
    108, 12, 11, 14, 13, 15, 10, 15, 12, 10,
    14, 13, 15, 10
]

# Z-score outlier detection
def detect_outliers(data, threshold=3):
    mean = np.mean(data)
    std = np.std(data)
    return [i for i in data if np.abs((i - mean) / std) > threshold]

print("Outliers:", detect_outliers(dataset))
