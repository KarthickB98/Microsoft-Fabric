# 🚖 NYC Green Taxi Data Engineering Project (Microsoft Fabric)

This project demonstrates a complete data engineering workflow using the NYC Green Taxi dataset in Microsoft Fabric. It includes ingestion, transformation, dimension modeling, and reporting—all driven by pipeline automation and Lakehouse architecture.

## 📦 Dataset

- **Source:** NYC TLC Green Taxi Trip Data  
- **Month Processed:** January 2025 (initial load)  
- **Format:** Parquet  
- **Schema Includes:** pickup & drop-off timestamps, passenger count, trip distance, total amount, payment type, vendor, location IDs.

## 🧱 Architecture

- **Lakehouse Zones:**  
  - *Raw (Bronze):* Unprocessed drop of source file  
  - *Cleaned (Silver):* Transformed trips with basic filtering & typing  
  - *Dimensional (Gold):* Star schema-ready tables for reporting

- **Star Schema Tables:**
  - `Trips` (Fact)
  - `Zones`, `PaymentTypes`, `Vendors` (Dimensions)

- **Pipeline Activities:**
  1. File ingestion from data lake
  2. Data cleaning via notebook
  3. Table partitioning and transformation
  4. Model view generation for reporting
  5. Trigger-based reload support for new months (e.g., February)

## 🛠️ Tools & Technologies

- [Microsoft Fabric](https://learn.microsoft.com/fabric/)  
- Notebooks (PySpark)
- Lakehouse (Delta/Parquet)
- Data Pipelines
- Power BI (for dashboards)

## 🚀 Getting Started

1. Download January Green Taxi data from the [NYC TLC Trip Record Data page](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
2. Upload to Fabric Lakehouse `/raw/greentaxi/2023/01/`
3. Trigger the pipeline or run the notebook for transformation
4. Explore transformed views or build Power BI dashboards

## 🔄 Future Enhancements

- Parameterized pipeline for dynamic monthly ingestion
- Automatic zone lookups using NYC taxi zone reference file
- Integration with REST API or Azure Logic Apps for real-time automation

---

**📊 Goal:** Validate an end-to-end Fabric pipeline—from raw ingestion to report-ready data—using a real-world dataset.

