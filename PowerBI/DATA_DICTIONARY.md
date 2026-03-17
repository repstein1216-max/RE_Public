# Data Dictionary

Field definitions for all datasets used in the RE_Public Power BI reports.

---

## property_sales.csv

Historical property sales records.

| Field | Type | Description |
|-------|------|-------------|
| `sale_id` | String | Unique identifier for the sale transaction |
| `sale_date` | Date (YYYY-MM-DD) | Date the sale closed |
| `list_date` | Date (YYYY-MM-DD) | Date the property was listed |
| `address` | String | Street address of the property |
| `city` | String | City |
| `state` | String | Two-letter state code (e.g., `CA`) |
| `zip_code` | String | Five-digit ZIP code |
| `neighborhood` | String | Neighborhood or subdivision name |
| `property_type` | String | One of: `Single Family`, `Condo`, `Multi-Family`, `Land`, `Townhouse` |
| `bedrooms` | Integer | Number of bedrooms |
| `bathrooms` | Decimal | Number of bathrooms (e.g., `2.5`) |
| `sq_ft` | Integer | Finished living area in square feet |
| `lot_size_sqft` | Integer | Lot size in square feet (0 for condos) |
| `year_built` | Integer | Year the property was constructed |
| `list_price` | Decimal | Original listing price in USD |
| `sale_price` | Decimal | Final sale price in USD |
| `days_on_market` | Integer | Number of days from list date to contract date |
| `price_per_sqft` | Decimal | `sale_price / sq_ft` |
| `list_to_sale_ratio` | Decimal | `sale_price / list_price` (e.g., `0.98` = 98%) |
| `agent_name` | String | Listing agent full name |
| `brokerage` | String | Listing brokerage name |

---

## market_summary.csv

Aggregated monthly market statistics.

| Field | Type | Description |
|-------|------|-------------|
| `year_month` | String (YYYY-MM) | Year and month of the summary period |
| `zip_code` | String | Five-digit ZIP code |
| `neighborhood` | String | Neighborhood or area name |
| `property_type` | String | Property type category |
| `active_listings` | Integer | Number of active listings at month end |
| `new_listings` | Integer | New listings added during the month |
| `closed_sales` | Integer | Number of sales that closed during the month |
| `pending_sales` | Integer | Number of sales under contract at month end |
| `median_list_price` | Decimal | Median listing price of active listings |
| `median_sale_price` | Decimal | Median closed sale price |
| `avg_days_on_market` | Decimal | Average days on market for closed sales |
| `avg_list_to_sale_ratio` | Decimal | Average list-to-sale price ratio |
| `months_of_supply` | Decimal | `active_listings / closed_sales` (inventory metric) |

---

## rental_listings.csv

Rental listing data for the rental market dashboard.

| Field | Type | Description |
|-------|------|-------------|
| `listing_id` | String | Unique identifier for the rental listing |
| `list_date` | Date (YYYY-MM-DD) | Date the rental was listed |
| `address` | String | Street address |
| `city` | String | City |
| `state` | String | Two-letter state code |
| `zip_code` | String | Five-digit ZIP code |
| `neighborhood` | String | Neighborhood or area name |
| `property_type` | String | One of: `Single Family`, `Condo`, `Multi-Family`, `Townhouse` |
| `bedrooms` | Integer | Number of bedrooms |
| `bathrooms` | Decimal | Number of bathrooms |
| `sq_ft` | Integer | Finished living area in square feet |
| `monthly_rent` | Decimal | Asking monthly rent in USD |
| `rent_per_sqft` | Decimal | `monthly_rent / sq_ft` |
| `is_vacant` | Boolean | `TRUE` if currently vacant, `FALSE` if occupied |
| `estimated_property_value` | Decimal | Estimated market value of the property |
| `annual_rental_yield` | Decimal | `(monthly_rent * 12) / estimated_property_value` |

---

## Notes

- All monetary values are in **US Dollars (USD)**.
- Dates use **ISO 8601 format** (`YYYY-MM-DD`).
- Boolean fields use `TRUE` / `FALSE` text values.
- Sample data is randomly generated for demonstration purposes only.
