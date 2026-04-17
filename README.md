# finance-data-portfolio

**My Journey from Beginner to Finance Quant Professional**  
Building real-world skills in **Financial Data Analysis → Data Science → Machine Learning → Quantum Computing** applied to finance.

Hello! I'm BOSI, an aspiring **Data Analyst → Data Scientist → ML Engineer → Quantum Finance Engineer**. 

This repository showcases my hands-on portfolio projects. I started as a complete beginner with no prior experience in coding or finance data work. Every project includes:
- Full end-to-end pipeline (raw data ingestion → cleaning → analysis → visualization)
- Well-documented code with explanations
- Beautiful visualizations
- LinkedIn-style article drafts (in the `docs/` folder)

My goal is to land roles in financial data analysis while building toward advanced quant and quantum finance applications.

## Tech Stack (Growing with Each Project)
- **Languages**: Python (Pandas, NumPy)
- **Data Sources**: yfinance, Alpha Vantage, Polygon.io, Kaggle NSE datasets
- **Visualization**: Plotly, Matplotlib, Seaborn
- **Tools**: Google Colab (cloud environment – no local installs needed)
- **Future**: Streamlit dashboards, Scikit-learn, PyTorch, Qiskit/PennyLane for quantum optimization

## Project Roadmap

| Project | Title | Focus Area | Key Skills | Status | Notebook Link |
|---------|-------|------------|------------|--------|---------------|
| 1 | Exploratory Financial Data Analysis | Data Analysis | Raw ingestion, cleaning, EDA, financial metrics, visualizations | In Progress | [project_01_eda_financial_analysis/notebooks/](project_01_eda_financial_analysis/notebooks/) |
| 2 | Automated Stock & Portfolio Dashboard | Data Analysis + Visualization | Dashboarding, API integration | Planned | Coming soon |
| 3 | Classical Risk & Portfolio Optimization | Data Science | Markowitz model, Monte Carlo, VaR | Planned | Coming soon |
| 4 | Time-Series Forecasting & ML Trading Signals | Machine Learning | LSTM, XGBoost, backtesting | Planned | Coming soon |
| 5 | Reinforcement Learning Trading Bot | ML Engineering | Stable-Baselines3, algorithmic trading | Planned | Coming soon |
| 6 | Quantum Portfolio Optimization | Quantum Computing in Finance | QUBO, QAOA simulation with Qiskit | Planned | Coming soon |
| Bonus | NSE Kenya Market Analysis | Local Market Relevance | Cleaning real Kenyan stock data | Planned | [nse_kenya_data/](nse_kenya_data/) |

*Projects are built progressively — each one reuses code from the previous and adds new skills.*

## Why Finance + Local Focus?
I am particularly interested in applying these skills to both global markets and the **Nairobi Securities Exchange (NSE)**. Kenya's market offers unique opportunities for data-driven insights in emerging economies. One bonus project will use the comprehensive NSE historical dataset (2007–2025) available on Kaggle for realistic cleaning and analysis practice.

## LinkedIn Articles
I will write and publish an article after completing each project. Drafts will live in the `docs/` folder. These articles explain the "why", the challenges I faced as a beginner, and the business value of the analysis.

## Learning Approach
- Everything is explained from first principles (no assumed knowledge).
- Full data pipeline mindset: ingestion → quality checks → cleaning → feature engineering → export → insights.
- Code is clean, commented, and reproducible in Google Colab.

## How to Explore This Repo
1. Start with this README for the big picture.
2. Go into each `project_XX_` folder and read its own `README.md`.
3. Open the notebooks directly on GitHub (or better, open them in Google Colab via the "Open in Colab" badge I'll add).
4. Check the `figures/` folders for visualizations.

---

## Folder Structure
```
finance-data-portfolio/
├── README.md                  # Main portfolio overview + navigation
├── requirements.txt           # All dependencies
├── .env                       # API keys (never to be committed) (to use with vscode)
├── .gitignore                 # to use with vscode)
├── data_pipeline/             # Reusable code
│   ├── __init__.py
│   ├── data_ingestion.py      # Functions for yfinance, Alpha Vantage, etc.
│   ├── data_cleaning.py       # Cleaning, validation, feature engineering
│   ├── data_storage.py        # Save to CSV, Parquet, SQLite
│   └── utils.py               # Helpers (logging, config)
├── project_01_eda_financial_analysis/   # Each project in its own folder
│   ├── notebooks/
│   │   ├── 01_raw_ingestion.ipynb
│   │   ├── 02_data_cleaning.ipynb
│   │   └── 03_eda_visualization.ipynb
│   ├── data/
│   │   ├── raw/               # Never commit large raw files → use .gitignore
│   │   ├── processed/         # Clean Parquet/CSV
│   │   └── external/          # Kaggle downloads, etc.
│   ├── src/                   # Reusable scripts for this project
│   ├── figures/               # Plots for LinkedIn & README
│   ├── reports/               # Analysis summaries
│   └── README.md              # Project-specific README
├── project_02_dashboard/      # And so on for all 6–8 projects
├── nse_kenya_data/            # Special folder for local market data
└── docs/                      # Extra docs or LinkedIn article drafts
```
