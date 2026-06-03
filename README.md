# Global Happiness Dataset Analysis

## Overview

This project performs **Exploratory Data Analysis (EDA)** on the Global Happiness Dataset using Python. The objective is to analyze happiness scores across countries and understand how factors such as GDP, family support, health, freedom, generosity, and government trust contribute to overall happiness.

The project demonstrates data cleaning, statistical analysis, ranking of countries, and data visualization using Pandas, NumPy, Matplotlib, and Seaborn.

---

# Dataset Information

The dataset contains information about happiness rankings and scores for countries around the world.

### Dataset Features

| Column Name                   | Description                       |
| ----------------------------- | --------------------------------- |
| Country                       | Country Name                      |
| Region                        | Geographic Region                 |
| Happiness Rank                | Global Happiness Ranking          |
| Happiness Score               | Overall Happiness Score           |
| Standard Error                | Standard Error of Happiness Score |
| Economy (GDP per Capita)      | Economic Contribution             |
| Family                        | Family/Social Support             |
| Health (Life Expectancy)      | Health Index                      |
| Freedom                       | Freedom to Make Life Choices      |
| Trust (Government Corruption) | Perceived Government Trust        |
| Generosity                    | Generosity Score                  |
| Dystopia Residual             | Residual Happiness Factor         |
| year                          | Year of Observation               |

---

# Technologies Used

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

# Data Preprocessing

## Handling Missing Values

```python
df.dropna(inplace=True)
```

Rows containing missing values were removed from the dataset.

### Result

* Original Records: 1231
* Clean Records: 158

---

## Duplicate Removal

```python
df.drop_duplicates(inplace=True)
```

Duplicate entries were checked and removed.

---

## Dataset Information

```python
df.info()
```

### Summary

* Total Records: 158
* Total Features: 14
* Numeric Columns: 12
* Categorical Columns: 2

---

# Statistical Analysis

```python
df.describe().round(3)
```

### Key Statistics

| Metric                  | Value |
| ----------------------- | ----- |
| Mean Happiness Score    | 5.376 |
| Median Happiness Score  | 5.232 |
| Maximum Happiness Score | 7.587 |
| Minimum Happiness Score | 2.839 |
| Mean GDP per Capita     | 0.846 |
| Mean Health Score       | 0.630 |

---

# Top 10 Happiest Countries

| Country     | Happiness Score |
| ----------- | --------------- |
| Switzerland | 7.587           |
| Iceland     | 7.561           |
| Denmark     | 7.527           |
| Norway      | 7.522           |
| Canada      | 7.427           |
| Finland     | 7.406           |
| Netherlands | 7.378           |
| Sweden      | 7.364           |
| New Zealand | 7.286           |
| Australia   | 7.284           |

---

# Bottom 10 Least Happy Countries

| Country      | Happiness Score |
| ------------ | --------------- |
| Togo         | 2.839           |
| Burundi      | 2.905           |
| Syria        | 3.006           |
| Benin        | 3.340           |
| Rwanda       | 3.465           |
| Afghanistan  | 3.575           |
| Burkina Faso | 3.587           |
| Ivory Coast  | 3.655           |
| Guinea       | 3.656           |
| Chad         | 3.667           |

---

# Regional Distribution

| Region                          | Number of Countries |
| ------------------------------- | ------------------- |
| Sub-Saharan Africa              | 40                  |
| Central and Eastern Europe      | 29                  |
| Latin America and Caribbean     | 22                  |
| Western Europe                  | 21                  |
| Middle East and Northern Africa | 20                  |
| Southeastern Asia               | 9                   |
| Southern Asia                   | 7                   |
| Eastern Asia                    | 6                   |
| North America                   | 2                   |
| Australia and New Zealand       | 2                   |

---

# Data Visualizations

## 1. Distribution of Happiness Scores

![Happiness Distribution](images/happiness_distribution.png)

### Insights

* Happiness scores are approximately normally distributed.
* Most countries fall between scores of 4 and 7.
* Very few countries have extremely high or extremely low happiness scores.

---

## 2. Countries per Region

![Countries per Region](images/countries_per_region.png)

### Insights

* Sub-Saharan Africa contains the highest number of countries.
* Western Europe and Latin America also contribute significantly.

---

## 3. Health vs Happiness Score

![Health vs Happiness](images/health_vs_happiness.png)

### Insights

* Countries with higher life expectancy generally report higher happiness scores.
* Positive correlation exists between health and happiness.

---

## 4. Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

### Insights

Strong positive correlations were observed between:

* Economy (GDP per Capita) and Happiness Score
* Family Support and Happiness Score
* Health and Happiness Score
* Freedom and Happiness Score

These factors appear to be major contributors to overall happiness.

---

# Key Findings

### Happiest Country

**Switzerland** ranked first with a happiness score of **7.587**.

### Least Happy Country

**Togo** ranked last with a happiness score of **2.839**.

### Important Happiness Factors

The strongest contributors to happiness are:

1. Economy (GDP per Capita)
2. Family Support
3. Health (Life Expectancy)
4. Freedom

### Regional Observation

Western European countries dominate the top happiness rankings, while several Sub-Saharan African countries appear among the lowest-ranked nations.

---

# Project Structure

```text
Global-Happiness-Analysis/
│
├── Global Happiness Dataset.csv
├── Happiness_Analysis.ipynb
├── README.md
│
└── images/
    ├── happiness_distribution.png
    ├── countries_per_region.png
    ├── health_vs_happiness.png
    └── correlation_heatmap.png
```

---

# Installation

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

---

# Run the Project

```bash
jupyter notebook
```

Open:

```text
Happiness_Analysis.ipynb
```

and run all cells.

---

# Future Improvements

* Interactive Dashboard using Streamlit
* Year-wise Happiness Trend Analysis
* Country Comparison Dashboard
* Machine Learning Model for Happiness Prediction
* Geographical Visualization using Plotly Maps

---

# Author

Global Happiness Dataset Analysis Project

A Data Analytics and Visualization project developed using Python, Pandas, NumPy, Matplotlib, and Seaborn.
