# csai382_lab_2_4_<yourname>

This project is a small reproducible ETL pipeline built for a restaurant dataset. It loads two CSV files (`menu_items.csv` and `order_details.csv`), cleans and joins them, computes simple metrics, and logs the whole run.

## Project Structure

- `lab_2_4_repro_logging` – Databricks notebook with the ETL steps.
- `data/` – Input CSVs:
  - `menu_items.csv`
  - `order_details.csv`
- `logs/` – Log files created every time the notebook runs.
- `requirements.txt` – Python environment captured with `pip freeze`.
- `data_hashes.json` – SHA-256 hashes of the input CSVs.
- `RUN.md` – Exact steps to re-run the ETL.

## What the ETL Does

- Reads `menu_items.csv` and `order_details.csv` with Pandas.
- Cleans text fields, fixes dates, and normalizes time values.
- Joins orders to menu items.
- Creates a tidy table with order ID, date/time, item name, category, and price.
- Computes basic metrics such as:
  - Top items by quantity.
  - Revenue by category.
  - Busiest hour of the day.
- Saves metrics to a timestamped CSV file in the repo.

## Ethics Reflection

1. **What information should not be logged?**

   - Personal or sensitive data about customers (for example, names, phone numbers, or payment details), because logs can be shared or stored for a long time and could expose private information.
   - Secrets such as passwords, API keys, and access tokens, because if they appear in logs, anyone with log access could use them to get into systems or read protected data.

2. **How does reproducibility support accountability and fairness?**

   Reproducibility lets others rerun the same pipeline and confirm that it produces the same results with the same inputs and code. When models or analyses affect people, this makes it easier to detect errors or bias, explain how results were produced, and correct problems, which supports more accountable and fair use of data.
