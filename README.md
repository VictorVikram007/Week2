# Emission Factors Data Analysis

This project performs **exploratory data analysis (EDA)** and visualization on a dataset containing **supply chain emission factors**. It helps identify the most polluting industries and understand how categorical variables like `Substance`, `Unit`, and `Source` affect emission factors.

---

##  Dataset Overview

The dataset includes:

- `Substance`: Type of greenhouse gas (e.g., CO₂, Methane)
- `Unit`: Measurement units
- `Source`: Type of source (Commodity or Industry)
- `Supply Chain Emission Factors with Margins`: Target column (kg CO2e/unit)
- Additional columns: `Name`, `Code`, `Year` (used in analysis, later dropped)

---

##  Features of the Code

### 1.  Data Inspection
- Displays column names, data types, summary statistics, and missing values.

### 2.  Target Distribution Visualization
- Histogram with KDE plot
- Boxplot to show spread and outliers

### 3.  Categorical Mapping
- Encodes categorical columns (`Substance`, `Unit`, `Source`) into numerical form.

### 4.  Top Emitters Analysis
- Computes and visualizes the **top 10 industries** with the highest average emissions.

### 5.  Data Cleaning
- Drops unused columns like `Name`, `Code`, and `Year`.

### 6. Feature-Target Preparation
- Separates features (`X`) and target variable (`y`) for future modeling.

### 7.  Categorical Feature Analysis
- Bar plots showing **mean emissions** by each categorical feature.

### 8.  Pairwise Relationships
- `Pairplot` of numerical features to see relationships and distributions.

### 9.  Correlation Clustermap
- Generates a correlation heatmap with clustering, after cleaning `NaN` and `inf` values.

---

##  Error Handling
- Uses `.get()` and `errors='ignore'` to avoid `KeyError`s.
- Cleans correlation matrix before generating clustermap.
- Checks for presence of necessary columns before plotting.

---

## Requirements

- Python 3.x
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scipy` (for clustering)

You can install them using:

```bash
pip install pandas numpy matplotlib seaborn scipy
