# How to Run the ETL Notebook

## Prerequisites

- A Databricks workspace and a running cluster.
- This GitHub repository connected under **Repos** in Databricks.
- The CSV files placed in the `data/` folder in the repo:
  - `data/menu_items.csv`
  - `data/order_details.csv`

## Steps in Databricks

1. Go to **Repos** in Databricks and open this repository.
2. Open the notebook: `lab_2_4_repro_logging`.
3. Attach the notebook to a cluster and click **Run all** (or run cells from top to bottom).
4. After the run finishes:
   - A log file is created in `logs/` with a name like `run_YYYYMMDD_HHMM.log`.
   - `requirements.txt` is created or updated at the root of the repo.
   - `data_hashes.json` is created with SHA-256 hashes for `menu_items.csv` and `order_details.csv`.
   - A metrics file is saved to `data/metrics_<timestamp>.csv`.

## Optional: Run locally

If you want to run this locally instead of Databricks:

1. Clone the repo and create a virtual environment.
2. Install dependencies (after one Databricks run has created `requirements.txt`):
   - `pip install -r requirements.txt`
3. Open the notebook in Jupyter or VS Code and run all cells.
