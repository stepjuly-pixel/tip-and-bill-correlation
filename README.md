# Tip and Bill Correlation Analysis

## Project Overview

This project explores the relationship between tip amounts and total bill sizes using the classic `tips` dataset from the Seaborn library.
The goal is to determine whether the relationship between tips and bills is statistically significant, identify the most appropriate correlation method, and investigate how group size relates to total bill amount.

The project follows a structured analytical approach:

- Data loading and inspection

- Scatter plot visualization

- Pearson and Spearman correlation analysis

- Distribution analysis and normality assessment

- Group size vs total bill correlation

## Tools & Libraries

- Python

- Pandas

- Matplotlib

- Seaborn

- SciPy (pearsonr, spearmanr)

## Dataset

The project uses the built-in Seaborn `tips` dataset containing 244 records with the following key columns:

- `total_bill` – total bill amount

- `tip` – tip amount

- `sex` – gender of the person paying

- `smoker` – whether the party included smokers

- `day` – day of the week

- `time` – lunch or dinner

- `size` – size of the dining party

## Analysis & Key Insights

### Tip vs Total Bill – Scatter Plot

- Visual inspection reveals a **positive relationship** between tip size and total bill.

- Most data points are concentrated in the lower-left region, with a few high-value outliers.

<img src="images/scatter_plot.png" width="550" />

### Pearson Correlation

- p-value < 0.05 — the relationship is **statistically significant**.

- Pearson correlation coefficient indicates a **moderate positive** linear relationship between tip and total bill.

### Spearman Correlation

- p-value < 0.05, coefficient < 0.7 — tip size and check size have a **statistically significant moderate direct relationship**.

- Spearman confirms the finding is robust regardless of distribution shape.

### Distribution Analysis

- The distribution of tips is **asymmetric and right-skewed**.

- The distribution of total bills is also **right-skewed**, but more symmetric.

- Since neither variable follows a normal distribution and outliers are present, **Spearman's method** is the more appropriate correlation measure for this data.

<img src="images/distributions.png" width="700" />

### Group Size vs Total Bill

- The `size` variable is discrete and non-normally distributed.

- Spearman correlation shows a **statistically significant moderate direct relationship** between group size and total bill.

- Larger groups tend to generate higher bills, but the relationship is moderate — not deterministic.

<img src="images/size_distribution.png" width="550" />

## How to Run

1. Clone this repository

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open [`Tip_and_Bill_Correlation.ipynb`](Tip_and_Bill_Correlation.ipynb) in Jupyter Notebook or Google Colab

## Project Structure

```
tip-and-bill-correlation/
├── images/
│   ├── scatter_plot.png
│   ├── distributions.png
│   └── size_distribution.png
├── Tip_and_Bill_Correlation.ipynb
├── requirements.txt
└── README.md
```
