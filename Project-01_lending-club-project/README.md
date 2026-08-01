# Lending Club Loan Performance Analysis
 
Exploratory data analysis of Lending Club's historical loan data (2007–2018), looking at which loans perform well and which don't. This was built as part of my journey into being a future Qunatum Fintech Engineer. This project is part of a larger series, moving from Excel/SQL/Power BI fundamentals toward more advanced data science and quant applications.

see the [main portfolio repo](https://github.com/BunnyeNyash/finance-data-portfolio.git) for other projects.
 
## Project Goal
 
Using real-world peer-to-peer lending data, this project answers:
- What does "loan performance" actually mean in this dataset (paid off, defaulted, late, etc.)?
- Which loan characteristics (grade, interest rate, purpose, income, debt-to-income ratio) are associated with better or worse performance?
- Can a simple, explainable risk-tier system (Low / Medium / High) meaningfully separate good loans from bad ones?

 
## Dataset
 
**Source:** [All Lending Club loan data](https://www.kaggle.com/datasets/wordsforthewise/lending-club) (Kaggle)
 
Contains accepted and rejected loan applications from 2007–2018. This project uses only the **accepted loans** file, since it's the only one with an actual outcome (`loan_status`). The rejected-loans file only has application-time data and no performance history.
 
The full file is several GB with 2M+ rows and 151 columns; this project works with a sample (10,000–200,000 rows) for tractability.
 
> **Note:** Raw data is not included in this repo (see `.gitignore`) due to file size and Kaggle's terms of use. See [Setup](#setup) below for how to download it yourself.

## Project Structure
```
lending-club-project/
│
├── README.md
├── requirements.txt
├── .gitignore
├── .env                          # Kaggle credentials, etc. — never committed
│
├── notebooks/
│   ├── 01_raw_ingestion.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── 03_eda_visualization.ipynb
│
├── data/
│   ├── raw/                      # untouched sample, straight from Kaggle
│   ├── processed/                # cleaned dataset, output of notebook 2
│   └── external/                 # any extra reference data (e.g. data dictionary)
│
├── figures/                      # saved charts/plots for README & LinkedIn post
│
└── reports/                      # written summary of findings
```

## Methodology
 
1. **Raw Ingestion** — Download the dataset via the Kaggle API, load a sample, and run sanity checks: shape, dtypes, missing values, and the distribution of `loan_status`.
2. **Data Cleaning** — Handle missing values column by column, fix data types, collapse `loan_status` into a `Good` vs. `Bad` performance flag, drop irrelevant or leakage-prone columns, and engineer a few additional features (e.g. income-to-loan ratio).
3. **EDA & Visualization** — Compute default rates by grade, purpose, state, and term; visualize interest rate vs. risk; and build a rule-based risk-tier segmentation, validated against actual default rates.
   
## Setup
 
1. Clone this repo:
```bash
   git clone https://github.com/BunnyeNyash/finance-data-portfolio/Project-01_lending-club-project.git
   cd Project-01_lending-club-project
```
 
2. Install dependencies:
```bash
   pip install -r requirements.txt
```
 
3. Get a Kaggle API key from [kaggle.com/settings](https://www.kaggle.com/settings) → **Create New Token**.
4. Create a `.env` file in the project root:
```
   KAGGLE_USERNAME=your_kaggle_username
   KAGGLE_KEY=your_kaggle_api_key
```
   (`.env` is gitignored — never commit this file.)
 
5. Run the notebooks in order: `01_raw_ingestion.ipynb` → `02_data_cleaning.ipynb` → `03_eda_visualization.ipynb`.
   
## Tech Stack
 
- **Language:** Python (pandas, numpy)
- **Visualization:** Matplotlib, Seaborn, Plotly
- **Data Source:** Kaggle API
- **Environment:** Google Colab / Jupyter
  
## Key Findings
 
*(To be filled in once the analysis is complete.)*
 
## License
 
Data is provided by Lending Club via Kaggle, subject to Kaggle's terms of use. This repo's code is available under the MIT License.
