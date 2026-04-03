# Kaggle EDA

A collection of exploratory data analysis notebooks for Kaggle datasets.

## Project structure

```
├── data/                        # Raw CSV datasets
├── notebooks/                   # EDA notebooks (one folder per dataset)
│   ├── energy-economics-curated/
│   ├── axp-time-series-stock-data-19722026/
│   ├── global-war-and-conflict-impact-dataset-19502024/
│   ├── pokemon-complete-stats-gen-1-to-gen-9/
│   └── toyota-stock-market-intelligence/
├── credentials.json             # Kaggle API token (not tracked)
└── .gitignore
```

## Datasets

| # | Dataset | Notebook | Kaggle link |
|---|---------|----------|-------------|
| 1 | Toyota Stock Market Intelligence (1980–2026) | `notebooks/toyota-stock-market-intelligence/toyota-stock-eda.ipynb` | [link](https://www.kaggle.com/datasets/mdmahfuzsumon/toyota-stock-market-intelligence-19802026/data) |
| 2 | Energy Economics Curated Dataset | `notebooks/energy-economics-curated/energy-economics-eda.ipynb` | [link](https://www.kaggle.com/datasets/sandhyapalaniappan/energy-economics-curated-dataset) |
| 3 | AXP Time Series Stock Data (1972-2026) | `notebooks/axp-time-series-stock-data-19722026/eda.ipynb` | [link](https://www.kaggle.com/datasets/borovai0/axp-time-series-stock-data-19722026) |
| 4 | Pokemon Complete Stats (Gen 1-9) | `notebooks/pokemon-complete-stats-gen-1-to-gen-9/eda.ipynb` | [link](https://www.kaggle.com/datasets/ibrahimqasimi/pokemon-complete-stats-gen-1-to-gen-9) |
| 5 | Global War & Conflict Impact (1950-2024) | `notebooks/global-war-and-conflict-impact-dataset-19502024/eda.ipynb` | [link](https://www.kaggle.com/datasets/khushikyad001/global-war-and-conflict-impact-dataset-19502024) |

## Setup

1. Copy your Kaggle API token into `credentials.json`:

   ```json
   {
     "kaggle_api_token": "<your-token>"
   }
   ```

2. Export it as an environment variable:

   ```bash
   export KAGGLE_API_TOKEN=$(jq -r .kaggle_api_token credentials.json)
   ```

3. Download a dataset:

   ```bash
   kaggle datasets download -d <owner>/<dataset> -p data/ --unzip
   ```
