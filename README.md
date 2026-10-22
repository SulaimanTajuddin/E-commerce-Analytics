# E-commerce-Analytics

Exploratory data analysis of e-commerce orders and transactions using the Kaggle dataset in `ecommerce_orders_transactions_2026.csv`.

## Project files

- `ecommerce_orders_transactions_2026.csv` — source dataset.
- `ecommerce_eda.ipynb` — executed Jupyter notebook containing the analysis, tables, and visualizations.

## Run the analysis

Open `ecommerce_eda.ipynb` in Jupyter or VS Code with a Python 3 kernel. Keep the CSV in the project directory so the notebook can load it by its relative path. The notebook uses `pandas`, `numpy`, `matplotlib`, and `seaborn`.

## Analysis

The notebook examines data structure and completeness, sales and profit metrics, monthly trends, product and category performance, customer and market segments, discounts, returns, delivery, and correlations. It uses distinct `Order_ID` counts for order totals and distinguishes `Net_Sales_USD` from `Total_Order_Value_USD`.

### Snapshot findings

- The dataset contains **200,000 rows** and **50 columns**, with order dates from January 1 through December 31, 2026.
- Total net sales are approximately **USD 105.74 million**, total order value is **USD 125.48 million**, and order profit is **USD 30.49 million**.
- There is one row per distinct order. Average **net sales per order** are approximately **USD 528.70**; average **total order value** is approximately **USD 627.39**. The latter uses `Total_Order_Value_USD`, which equals net sales plus tax and shipping in the CSV, so it should not be confused with net-sales AOV.
- November has the highest monthly net sales in this dataset, at approximately **USD 11.62 million**.

### Data considerations

- The date range includes dates later than October 22, 2026. Confirm whether records after the current analysis date are expected (for example, forecast or synthetic data) before using time-based findings.
- `Return_Reason` and `Coupon_Code` are frequently blank and may only apply to returned or coupon-using orders.
- The `Order_Status` and `Return_Status` fields report different returned-row counts. The notebook includes a cross-tabulation; reconcile the field definitions before reporting a return rate.
- These figures are descriptive summaries of the supplied data. Validate field definitions and business rules before using them for external reporting or decisions.
