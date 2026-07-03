# Data Dictionary — Global Superstore

| Column | Type | Description |
|---|---|---|
| Row ID | int | Unique row identifier |
| Order ID | string | Unique order identifier (one order can span multiple rows/products) |
| Order Date | date (DD-MM-YYYY) | Date the order was placed |
| Ship Date | date (DD-MM-YYYY) | Date the order was shipped |
| Ship Mode | categorical | Same Day / First Class / Second Class / Standard Class |
| Customer ID | string | Unique customer identifier |
| Customer Name | string | Customer name |
| Segment | categorical | Consumer / Corporate / Home Office |
| City | string | Customer city |
| State | string | Customer state/province |
| Country | string | Customer country |
| Postal Code | string/float | Postal code (has missing values, esp. outside US) |
| Market | categorical | US / APAC / EU / LATAM / Africa / EMEA / Canada |
| Region | categorical | Sub-region within market (e.g., East, Oceania, North Asia) |
| Product ID | string | Unique product identifier |
| Category | categorical | Furniture / Office Supplies / Technology |
| Sub-Category | categorical | More granular product grouping |
| Product Name | string | Product description |
| Sales | float | Revenue for the line item (local currency, assumed USD) |
| Quantity | int | Units sold |
| Discount | float | Discount applied (0–1, e.g., 0.1 = 10%) |
| Profit | float | Profit for the line item (can be negative) |
| Shipping Cost | float | Cost to ship the order (note: has leading/trailing spaces in raw CSV) |
| Order Priority | categorical | Critical / High / Medium / Low |

## Known Data Quality Issues (found during initial audit)
- File encoding is non-UTF8 / extended ASCII — needs `encoding='latin1'`
  (or similar) on read.
- Date columns are strings in `DD-MM-YYYY` format, not native datetime.
- `Shipping Cost` has stray leading/trailing whitespace around numeric
  values — needs `.str.strip()` before casting to float.
- `Postal Code` has missing values (mostly non-US rows) — expected, not
  necessarily an error.
- Potential duplicate `Row ID`/`Order ID` combinations to verify.
