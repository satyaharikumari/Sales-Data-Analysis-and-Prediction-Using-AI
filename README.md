# Sales Data Analysis and Prediction Using AI

**Author:** Satya Hari Kumari\
**Level:** Beginner\
**Project type:** Data Analytics and Machine Learning

## Project description

This project analyzes historical online retail transactions and builds a
beginner-friendly Random Forest regression model to estimate monthly
revenue. It includes data cleaning, key performance indicators (KPIs),
visualizations, top-product and country analysis, model evaluation, and
CSV exports.

## Dataset

-   **Name:** UCI Online Retail
-   **Source page:**
    https://archive.ics.uci.edu/dataset/352/online+retail
-   **Direct Excel download:**
    https://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx
-   **Citation:** Chen, D. (2015). *Online Retail* [Dataset](#dataset).
    UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33
-   **License:** CC BY 4.0; attribute the dataset when sharing derived
    work.

The dataset records transactions from a UK-based online retailer between
December 2010 and December 2011. It is historical and should not be
treated as current market data.

## Technologies used

-   Python
-   Jupyter Notebook
-   pandas and NumPy for data preparation and analysis
-   Matplotlib for charts
-   scikit-learn for Random Forest regression and evaluation
-   openpyxl for reading the Excel dataset

## Files

-   `SatyaHari_SalesDataAnalysisAI.ipynb` --- complete analysis and
    model notebook
-   `requirements.txt` --- Python dependencies
-   `SatyaHari_ProjectReport.docx` --- project documentation

## Setup and run

1.  Install Python 3.10 or later.

2.  Download or clone the project folder.

3.  Open a terminal in the project folder.

4.  Install dependencies:

    ``` bash
    python -m pip install -r requirements.txt
    ```

5.  Start Jupyter:

    ``` bash
    jupyter notebook
    ```

6.  Open `SatyaHari_SalesDataAnalysisAI.ipynb` and choose **Kernel →
    Restart & Run All**.

The notebook attempts to download the Excel dataset from UCI. If this
fails, download `Online Retail.xlsx` from the dataset page, put it
beside the notebook, and run the notebook again.

## Methodology

1.  Load and inspect the raw transaction data.
2.  Remove duplicate rows, cancellations, missing essential fields, and
    non-positive quantities/prices.
3.  Calculate line revenue as `Quantity × UnitPrice`.
4.  Summarize revenue by month, product, and country.
5.  Build a chronological train/test split on monthly revenue.
6.  Train a Random Forest regressor using month, year, and
    previous-month revenue.
7.  Evaluate predictions with MAE, RMSE, and R-squared.

## Outputs

When the notebook runs successfully, it displays KPIs, charts, model
metrics, and actual-versus-predicted monthly revenue. It also exports: -
`monthly_sales_summary.csv` - `top_products_by_revenue.csv` -
`country_sales_summary.csv` - `actual_vs_predicted_monthly_sales.csv`

## Limitations

-   The data is historical (2010--2011), not current.
-   Revenue is not profit; costs are unavailable.
-   The forecast uses a small number of monthly observations and is
    intended for learning.
-   Results may vary with software versions or changes to data cleaning.
-   Missing customer IDs limit customer-level analysis.

## Reproducibility

The model uses `random_state=42` and a chronological split. Run all
notebook cells from top to bottom to regenerate the outputs.
