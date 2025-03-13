# Data Engineering Portfolio

Data Engineer Portfolio: Building a DWH for stock analysis using Python, PostgreSQL with ETL processes.

## About the Project
A Data Warehouse (DWH) for analyzing U.S. stock data (Microsoft, Nvidia, Meta, etc.) from the [Yahoo Finance API](https://pypi.org/project/yfinance/). Built using Bill Inmon’s approach, it processes 100k+ records (2000–2024) across STG, DDS, and CDM layers, with metadata triggers and three data marts for stock trends, dividends, and volatility.

### Key Features
- Extracts stock data (prices, dividends, balance sheets) via Yahoo Finance API.
- Implements an ETL pipeline with Python (Pandas, yfinance).
- Structures a PostgreSQL DWH: STG (raw), DDS (normalized), CDM (data marts).
- Logs metadata with triggers in the `core` schema.
- Data marts:
  - `stocks_stats_monthly`: Monthly price and volume trends.
  - `dividends_yearly`: Yearly dividend counts and totals.
  - `stocks_volatility_monthly`: Monthly volatility range and average close.

## Technologies
- **Python**: ETL pipeline (Pandas, yfinance).
- **PostgreSQL**: DWH storage, triggers, materialized views.
- **SQL**: DDL/DML, query optimization.

## Project Structure
- `dwh_sql/` — SQL scripts for DWH creation, triggers, and materialized views.
- `csv/` — Sample stock data from Yahoo Finance API.

**Also included:**
- `scripts_for_ddl.ipynb` — DDL scripts simplifying database setup.
- `er_diagram.pgerd` — Entity-Relationship diagram.
- `dwh_backup.sql` — Backup file for the DWH.
- `yfinance_stock_data_download.ipynb` — ETL notebook (PDF/HTML versions included).

## Next Steps
- Migrate to Google BigQuery for cloud-based scalability.
- Automate with Apache Airflow for scheduled ETL workflows.
