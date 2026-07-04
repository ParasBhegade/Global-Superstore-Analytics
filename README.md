#  `Global Superstore — Sales & Profitability Analysis`

An end-to-end data analytics project that turns ~51,000 raw retail
transactions into actionable business recommendations — built to mirror
how a real analytics team scopes, cleans, analyzes, and reports on data.

> **Business question:** Where is Global Superstore making and losing
> money, and what should it change to improve profitability?

## ` Project Structure`
```
global-superstore-analytics/
├── data/
│   ├── raw/              # original, untouched data
│   └── processed/        # cleaned data used for analysis
├── notebooks/            # Jupyter notebooks (cleaning + analysis)
├── visuals/               # exported chart images
├── report/                # written insights & recommendations
├── src/                   # reusable helper functions (optional)
├── PRD.md                 # problem statement & project scope
├── DATA_DICTIONARY.md     # column definitions
├── requirements.txt
└── README.md
```


## ` Dataset`
**Global Superstore** — order-level retail transactions (2011–2014)
across US, APAC, EU, LATAM, Africa, and Canada markets. ~51K rows, 24
columns including Sales, Profit, Discount, Shipping Cost, Category,
Region, Segment, and dates. See `DATA_DICTIONARY.md` for full column
definitions.

##  `Tools`
Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## ` How to Run`
```bash
pip install -r requirements.txt
jupyter notebook notebooks/
```

## `Author`
*Paras Bhegade*
