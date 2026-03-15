
# E-commerce Data Lakehouse Pipeline

## 📌 Project Overview
This project demonstrates the design and implementation of a **full-scale ETL pipeline** for an e-commerce dataset using a **Delta Lakehouse architecture**.  
The pipeline processes raw CSV data into **analytics-ready tables**, following the **Bronze → Silver → Gold** layering:

- **Bronze:** Raw ingested data
- **Silver:** Cleaned, standardized, and deduplicated data
- **Gold:** Dimension & Fact tables for analytics

The goal is to **enable scalable, reliable, and automated data processing** for downstream reporting and business intelligence.

---

## 🛠️ Tools & Technologies
- **Frameworks & Languages:** PySpark, SQL
- **Data Lakehouse:** Delta Lake (Bronze/Silver/Gold)
- **Data Storage:** CSV + Delta tables
- **Orchestration & Automation:** Databricks notebooks, multi-threaded execution
- **Data Validation:** Revenue reconciliation, duplicate checks, data profiling

---

## 📂 Repository Structure
├─ README.md # Project documentation
├─ scripts/ # PySpark ETL notebooks
│ ├─ bronze_ingestion.ipynb
│ ├─ silver_transformations.ipynb
│ ├─ gold_modeling.ipynb
│ └─ monitoring_pipeline.ipynb
├─ data/ # Raw CSV files
│ ├─ customers.csv
│ ├─ orders.csv
│ ├─ products.csv
│ └─ ...


---

## 🔄 ETL Pipeline Process
1. **Bronze Layer:**  
   - Raw CSV ingestion into Delta tables  
   - Added ingestion timestamp & source file tracking  

2. **Silver Layer (Transformations & Cleaning):**  
   - Trimmed strings, normalized text, standardized zip codes  
   - Deduplicated data and handled nulls & incorrect formats  
   - Generated derived columns (e.g., delivery delay, order month)  

3. **Gold Layer (Dimensional Modeling):**  
   - Created **Dimension Tables:** `dim_customers`, `dim_products`, `dim_sellers`, `dim_geography`, `dim_date`  
   - Created **Fact Table:** `fact_sales`  
   - Surrogate keys and placeholder handling for unmatched joins  

4. **Pipeline Monitoring:**  
   - Logs execution status, duration, and errors in a monitoring table  
   - Multi-threaded execution with retries  

5. **Validation:**  
   - Revenue reconciliation between Silver and Gold  
   - Duplicate and null checks on key tables  

---

## 📊 Key Highlights
- **5000+ records ingested and processed** with Delta Lake can be used to process big data projects.
- **Automated pipeline** with retry logic & logging  
- **Dimensional modeling** for analytics-ready datasets  
- **Data quality checks** included: duplicates, nulls, revenue validation  
- Full support for **downstream BI dashboards**  

---

## 🎯 Outcome & Use Cases
- Enterprise-grade **data lakehouse ETL pipeline** showcasing **data engineering best practices**  
- Analytics-ready tables for **sales performance, customer segmentation, and geospatial analysis**  
- Demonstrates ability to handle **big data, automation, and data validation**  

---

## 🔗 Next Steps 
- Adding **incremental processing** for near real-time updates  
- Connecting **Gold layer tables** to BI tools like Power BI or Tableau  

---

## 📝 Author
**Yash Sharma** – Data Engineering | Big Data | PySpark | Delta Lake
