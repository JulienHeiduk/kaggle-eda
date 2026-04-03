# Kaggle EDA

A collection of exploratory data analysis notebooks for Kaggle datasets.

## Project structure

```
├── data/                        # Raw CSV datasets
├── notebooks/                   # EDA notebooks (one folder per dataset)
│   ├── energy-economics-curated/
│   └── toyota-stock-market-intelligence/
├── credentials.json             # Kaggle API token (not tracked)
└── .gitignore
```

## Datasets

| # | Dataset | Notebook | Kaggle link |
|---|---------|----------|-------------|
| 1 | Toyota Stock Market Intelligence (1980–2026) | `notebooks/toyota-stock-market-intelligence/toyota-stock-eda.ipynb` | [link](https://www.kaggle.com/datasets/mdmahfuzsumon/toyota-stock-market-intelligence-19802026/data) |
| 2 | Energy Economics Curated Dataset | `notebooks/energy-economics-curated/energy-economics-eda.ipynb` | [link](https://www.kaggle.com/datasets/sandhyapalaniappan/energy-economics-curated-dataset) |

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
