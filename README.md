# gsyn-data-engineering-challenge-Mirdul-Kumar
This is for Gsynergy data engineering challenge
<br>
# GSynergy Data Engineering Challenge

## Project Overview
This project is a solution for the GSynergy Data Engineering Challenge. It involves designing and implementing an ELT pipeline to process raw data, perform schema inference, apply data quality checks, normalize hierarchical data, and aggregate fact data in a data warehouse.

## Technologies Used
- **Cloud Provider:** Azure 
- **Storage:** Azure data lake storage Zen2 (ADLS zen2)
- **Data Warehouse:** Databricks 
- **ETL/ELT Tools:** Azure Data Factory 
- **Transformation Framework:** dbt (Data Build Tool)
- **Scripting & Query Language:** Python, SQL
- **Version Control:** Git & GitHub
- **Documentation Tools:** dbdiagram.io / draw.io for ER diagrams

## Setup Instructions
1. Clone this repository:
   ```sh
   git clone https://github.com/MirdulKumar/gsyn-data-engineering-challenge-Mirdul-Kumar.git
   cd gsyn-data-engineering-challenge-Mirdul-Kumar
   ```
2. Set up cloud storage (Azure) and upload raw data.
3. Configure your data warehouse (Databricks).
4. Install required dependencies:
   ```sh
   pip install -r requirements.txt  # 
   ```
5. Update configuration files with your cloud credentials and storage locations.

## How to Run the Pipeline
1. Execute the raw data ingestion script:
   ```sh
   python scripts/load_raw_data.py
   ```
2. Run data quality checks:
   ```sh
   python scripts/data_quality_checks.py
   ```
3. Normalize hierarchical data:
   ```sh
   python scripts/normalize_hierarchy.py
   ```
4. Aggregate fact data into `mview_weekly_sales`:
   ```sh
   python scripts/aggregate_sales.py
   ```

## How to Validate the Output
1. Connect to the data warehouse and verify table structures:
   ```sql
   SELECT * FROM staging.hier_table;
   SELECT * FROM refined.mview_weekly_sales;
   ```
2. Check data quality reports for errors and inconsistencies.
3. Run test queries to confirm aggregations.
4. Review logs and debug any failures.

For any issues, refer to the logs generated in the `logs/` directory.

---

**Author:** Mirdul Kumar
**Contact:** kmirdu91@gmail.com
