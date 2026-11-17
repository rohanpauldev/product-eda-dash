# Online Retail EDA Dashboard

Course: Data Visualization for Product Design (CSDC0207), Dr. B R Ambedkar NIT Jalandhar

## What this is
An exploratory analysis of the public Online Retail dataset (UCI Machine Learning Repository), a UK online retailer's transactions from 1 Dec 2010 to 9 Dec 2011. It answers one product question: when, where and through which products does revenue come in?

## Files
- `product_eda_dash.ipynb` - the notebook (load, profile, clean, summarise, plot)
- `Online Retail.xlsx` - the dataset (not included; download it from the UCI repository and place it next to the notebook)
- `chart1_monthly_revenue.png` to `chart5_daily_sales.png` - charts saved by the notebook

## How to run
1. Install the packages: `pip install pandas numpy matplotlib seaborn openpyxl`
2. Put `Online Retail.xlsx` in the same folder as the notebook.
3. Open the notebook and choose Run All. No manual steps are needed.

## What the notebook does
1. Loads the data (541,909 rows, 8 columns) and checks types, missing values and duplicates.
2. Cleans it: drops duplicates, rows with no CustomerID or Description, and rows with Quantity or UnitPrice of 0 or below. 392,692 rows remain.
3. Adds Revenue (Quantity x UnitPrice), Month and Day columns.
4. Flags outlier orders with the 1.5 x IQR rule (kept, not deleted).
5. Draws five charts: monthly revenue, top 10 products, top 10 countries, order value distribution, sales by day of week.

## Key figures (after cleaning)
Total revenue 8,887,208.89 GBP, 18,532 orders, 4,338 customers, 1,469 outlier orders.

## Known limitations
The order-value histogram is dominated by a few very large orders, POSTAGE and Manual appear in the product chart, December 2011 is a partial month, and rows without CustomerID were removed.
