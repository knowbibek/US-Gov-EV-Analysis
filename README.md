# Electric Vehicle Registration Analysis

This repository contains a Google Colab notebook that performs an end-to-end analysis of electric vehicle (EV) registration data. The primary objective is to explore trends, vehicle types, and adoption patterns in government or public-sector EV registrations. While the included dataset may be state-specific, the analysis framework is designed to be applied to **any similar dataset** across regions or states.

---

## 📁 Data

The analysis is based on a dataset named `gov_spending.csv`, which contains details related to electric vehicle registrations. The dataset is expected to include the following columns (depending on source):

- `Model Year`  
- `Make`  
- `City`, `County`, `State`  
- `Electric Vehicle Type` (e.g., BEV, PHEV)  
- `Electric Range`  
- `Clean Fuel Eligibility`  
- `Base MSRP` and more

> You can source this data from state transportation agencies or government open data portals. For example:  
> https://catalog.data.gov/dataset/electric-vehicle-population-data

---

## ⚙️ Setup and Execution

1. Open the provided Google Colab notebook (e.g., `EV_Registration_Analysis.ipynb`).
2. When prompted, upload the `gov_spending.csv` file.
3. The notebook includes steps to install necessary libraries (`findspark`, `pyspark`, `graphviz`) and configure a Spark environment inside Colab.
4. Run each cell sequentially to perform the analysis.

---

## 📊 Analysis Performed

The notebook performs the following steps:

### ✅ Data Loading and Cleaning

- Reads the uploaded CSV into a PySpark DataFrame
- Cleans the data (e.g., drops missing or null values)

### 📈 Exploratory Data Analysis (EDA)

- Counts and visualizes data by:
  - `Make`
  - `Model Year`
  - `City`, `County`
  - `Electric Vehicle Type` (BEV vs. PHEV)
- Generates visualizations:
  - Top EV brands (bar chart)
  - Registrations by model year (line plot)
  - EV type distribution (pie chart)
  - Median electric range trend (line plot)

### 🔮 Forecasting

- Applies **Linear Regression** to project the following through 2027:
  - Total EV registrations per year
  - Median electric range
  - BEV share among all electric vehicles

---

## 📌 Key Visualizations and Outputs

- Tables showing EV registration counts by category (Make, Year, Type, etc.)
- Horizontal bar chart of top EV makes
- Line charts showing time-based trends
- Pie chart comparing BEV and PHEV distribution
- Forecast charts with predicted values through 2027

---

### 🔢 BEV Share Forecast

| Year   | Metric               | Value    |
|--------|----------------------|----------|
| 2024   | Actual BEV Share     | 0.906103 |
| 2025   | Predicted BEV Share  | 0.923310 |
| 2026   | Predicted BEV Share  | 0.940517 |
| 2027   | Predicted BEV Share  | 0.958724 |

- **Actual BEV Share**: Proportion of BEVs in the most recent complete year.
- **Predicted BEV Share**: Linear regression forecasts for upcoming years.
- Interpretation: BEVs are projected to dominate the electric vehicle landscape in coming years, phasing out PHEVs in government and fleet adoption.

---

## 📦 Dependencies

These packages are automatically installed in the Colab environment:

- `pyspark`  
- `findspark`  
- `pandas`  
- `matplotlib`  
- `graphviz`  
- `scikit-learn`

No setup is required beyond running the notebook in Colab. If using locally, install these packages via pip.

---

## 🧭 Workflow Diagram

The following graph summarizes the analysis pipeline implemented in the notebook:

```graphviz
digraph {
  rankdir="LR"
  A [label="CSV File\n(gov_spending.csv)"]
  B [label="Google Colab Notebook"]
  C [label="PySpark DataFrame"]
  D [label="Data Cleaning\n& Aggregation"]
  E [label="Exploratory Analysis\n(EDA)"]
  F [label="Visualizations\n(Matplotlib)"]
  G [label="Forecast Models\n(Linear Regression)"]
  H [label="Insights & Trends"]

  A -> B -> C -> D -> E -> F -> G -> H
}
