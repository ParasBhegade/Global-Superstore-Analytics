# Data Audit Notes — Global Superstore

## Dataset Overview
- Source: Global Superstore dataset
- Rows: 51,290 | Columns: 24
- Time period: From '01-01-2011' to '31-12-2014'
- Markets covered: ['US', 'APAC', 'EU', 'Africa', 'EMEA', 'LATAM', 'Canada']

## Data Quality Checks Performed
| Check | Result | Action Needed |
|---|---|---|
| Duplicate rows | 0 found | None |
| Postal Code missing | 41,296 nulls | Expected — non-US rows don't have postal codes. Leave as-is. |
| Order Date / Ship Date | Loaded as string (object) | Convert to datetime |
| Time Period | From '01-01-2011' to '31-12-2014'  | None |
| Shipping Cost | Checked Impossible values and White Spaces | Converted to numeric |
| Discount | Range 0.0–0.85 | Valid, no fix needed |
| Sales / Quantity | No negative or zero values found | Valid |
| Sub-Category values | Checked via value_counts(), all consistent | None |


## Key Early Finding
Roughly 1 in 4 orders (24.46%) lose money. When comparing discount
levels between profitable and unprofitable orders, a clear pattern
emerges: orders that lose money carry an average discount of 45%,
while profitable orders average just 4.3% — a difference of nearly
10x. This suggests heavy discounting may be a major driver of losses.

- 24.46% of all orders are unprofitable
- Avg discount on loss-making orders: 45%
- Avg discount on profitable orders: 4.3%