# Power BI – Real Estate Analytics

This folder contains Power BI report documentation, data files, and setup instructions for the RE_Public real estate analytics dashboards.

## Folder Structure

```
PowerBI/
├── README.md              # This file
├── DATA_DICTIONARY.md     # Field definitions for all datasets
└── data/
    ├── property_sales.csv # Historical property sales records
    ├── market_summary.csv # Monthly market-level statistics
    └── rental_listings.csv# Rental listing data
```

## Reports

### 1. Real Estate Market Overview
**File:** `RE_Market_Overview.pbix`

Provides a high-level snapshot of the real estate market, including:
- Median sale price (monthly and YoY comparison)
- Average days on market
- List-to-sale price ratio
- Active and closed listing counts
- Geographic heat map by zip code

**Filters:** Date range, property type, zip code

---

### 2. Property Sales Analysis
**File:** `RE_Sales_Analysis.pbix`

Drill-through report for detailed sales data:
- Sales volume by property type (Single Family, Condo, Multi-Family, Land)
- Price per square foot distribution
- Bedroom/bathroom breakdown
- Neighborhood-level comparisons
- Top-selling agents and brokerages

**Filters:** Date range, property type, bedrooms, price range, neighborhood

---

### 3. Price Trends
**File:** `RE_Price_Trends.pbix`

Trend analysis and forecasting:
- Month-over-month median price change
- Year-over-year % change
- Price trend by neighborhood
- 12-month price forecast using linear regression

**Filters:** Date range, property type, neighborhood

---

### 4. Rental Market Summary
**File:** `RE_Rental_Summary.pbix`

Rental market performance metrics:
- Average monthly rent by bedroom count
- Rent per square foot by neighborhood
- Vacancy rates
- Rental yield (annual rent / property value)

**Filters:** Date range, bedroom count, neighborhood

---

## Setup Instructions

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) (free)
- Microsoft account (to publish to Power BI Service)

### Loading Sample Data

1. Open Power BI Desktop.
2. Open a `.pbix` file from this folder.
3. In the **Home** ribbon, click **Transform data** → **Data source settings**.
4. Update the file path to point to the CSV files in `data/`.
5. Click **Refresh** to load the data.

### Publishing to Power BI Service

1. In Power BI Desktop, click **Home** → **Publish**.
2. Select your Power BI workspace.
3. Click **Publish** and sign in if prompted.
4. Open [app.powerbi.com](https://app.powerbi.com) to view and share your report.

---

## Data Refresh

For live data, replace CSV data sources with a database or API connection:
- **SQL Server / Azure SQL** – Use the built-in SQL Server connector.
- **SharePoint / Excel** – Use the SharePoint Online List or Excel connector.
- **API** – Use Power Query's Web connector or a custom connector.

Schedule automatic refreshes in Power BI Service under **Dataset settings → Scheduled refresh**.
