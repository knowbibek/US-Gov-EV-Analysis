# US Government Electric Vehicle Spending Analysis

This project performs an exploratory data analysis (EDA) on a dataset detailing US government spending, specifically focusing on the procurement and analysis of electric vehicles. The analysis aims to identify trends, distributions, and key insights regarding EV adoption within government fleets.

## Technologies Used

*   Apache Spark (PySpark)
*   Python
*   Jupyter Notebook
*   Pandas
*   Matplotlib
*   Graphviz
*   Git & GitHub

## Setup and Installation

This project was developed and run in a Google Colab environment. To replicate the analysis, you will need:

1.  A Google Account to access Google Colab.
2.  The `gov_spending.csv` dataset. **[Specify how to obtain the dataset - e.g., "The dataset is included in this repository."]**

The Jupyter notebook includes cells to install the necessary dependencies (Java, Spark, findspark) within the Colab environment using shell commands.

If running this project locally, you will need to:

*   Install Java (OpenJDK 8 or later recommended).
*   Download and set up Apache Spark.
*   Install Python and the required libraries (`pyspark`, `findspark`, `pandas`, `matplotlib`, `graphviz`) using pip:

*   Set the `JAVA_HOME` and `SPARK_HOME` environment variables to point to your Java and Spark installations respectively.

## Usage

1.  Upload the `gov_spending.csv` file to your environment (e.g., to your Google Drive if using Colab, or place it in the same directory as the notebook if running locally).
2.  Open the `[your_notebook_name].ipynb` file (replace with your actual filename, e.g., `US_Gov_EV_Analysis.ipynb`) in Jupyter Notebook or Google Colab.
3.  Run the cells sequentially. The notebook performs the following steps:
    *   Installs dependencies (if in environments like Colab).
    *   Initializes a Spark session.
    *   Loads and cleans the data.
    *   Performs exploratory data analysis on various columns (Make, Model Year, City, Electric Vehicle Type, County).
    *   Generates visualizations (specifically a bar chart for top makes).
    *   Creates a data pipeline diagram.

## Data

The analysis uses a dataset named `gov_spending.csv`. This file contains records related to US government spending on vehicles, including details such as Make, Model Year, City, County, Electric Vehicle Type, and more. **[Add any other relevant details about the data source or specific columns if needed.]**

## Analysis & Findings

The notebook performs analysis on several aspects of the data, including:

*   Identifying the most common electric vehicle makes purchased by the government.
*   Analyzing the distribution of vehicles by model year.
*   Determining the cities and counties with the highest number of reported electric vehicles in the dataset.
*   Categorizing the types of electric vehicles.

Key visualizations highlight the distribution of top vehicle makes, providing insights into the most commonly procured EV brands by the US government within the scope of this dataset.

## Project Structure / Pipeline

A visual representation of the data analysis pipeline, from raw data ingestion and cleaning to analysis and visualization, is generated within the notebook using Graphviz.


DataSe(gov_spending.csv): https://catalog.data.gov/dataset/electric-vehicle-population-data
