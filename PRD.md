# Project Requirements Document (PRD)
## Global Superstore — Sales & Profitability Analysis

### 1. Background
Global Superstore is a fictional global retailer operating across multiple
markets (US, APAC, EU, LATAM, Africa, Canada). The dataset contains ~51,000
order-level transactions from 2011–2014, including sales, profit, discount,
shipping cost, and customer/product/geography attributes.

### 2. Business Problem
> Despite steady revenue growth, leadership suspects profit is not growing
> at the same rate. They want to know **where the company makes money,
> where it loses money, and why** — so they can fix pricing, discounting,
> and operational decisions.

### 3. Objectives
- Identify which markets, regions, segments, and categories drive the most
  revenue vs. the most profit (they are not always the same).
- Quantify the relationship between discounting and profitability.
- Understand shipping cost / ship mode impact on margins.
- Surface time-based trends (seasonality, YoY growth).
- Flag underperforming products/sub-categories worth discontinuing or
  re-pricing.

### 4. Success Criteria (what "done" looks like)
- Clean, reproducible dataset with documented cleaning decisions.
- 5–8 high-quality visualizations, each tied to a specific business
      question.
- A written insights report with concrete, prioritized recommendations
      (not just "sales are up/down").
- A public-facing README that explains the project in under 2 minutes
      of reading.

### 5. Key Questions to Answer
1. Which Region/Market/Segment/Category combinations are most profitable?
   Which are losing money?
2. Does discount level correlate with lower profit? At what discount
   threshold does profit typically turn negative?
3. Which Sub-Categories should be prioritized, re-priced, or dropped?
4. How does Ship Mode affect shipping cost and delivery-to-order profit?
5. What do sales and profit trends look like over time (monthly/yearly)?
   Any seasonality?
6. Who are the top customers/products by profit contribution (Pareto —
   is 80% of profit from 20% of products)?

### 6. Scope
**In scope:** descriptive & diagnostic analysis (what happened, why),
static visualizations, a written report.
**Out of scope:** predictive modeling/forecasting, live dashboards,
real-time data pipelines. (Could be a fast-follow phase 2.)

### 7. Deliverables
| Deliverable | Location |
|---|---|
| Cleaned dataset | `data/processed/` |
| Analysis notebook | `notebooks/` |
| Visualizations | `visuals/` |
| Insights & recommendations report | `report/` |
| Project README | `README.md` |

### 8. Tools
Python, Pandas, NumPy, Matplotlib/Seaborn, Jupyter Notebook.

### 9. Timeline (self-paced phases)
See `README.md` → Project Phases.
