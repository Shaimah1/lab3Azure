What I Did:
1. ✅ Connected to Azure Data Lake Storage
2. ✅ Loaded Silver layer data (books, authors, reviews)
3. ✅ Cleaned reviews data:
   - Removed null values
   - Filtered ratings (1-5 only)
   - Removed short reviews
   - Fixed date formats
4. ✅ Built Gold layer by joining all datasets
5. ✅ Added features like review length and average ratings
6. ✅ Saved as Delta table for analytics

How I Did It:
- Used Databricks notebooks with PySpark
- Connected to ADLS using storage account key
- Applied data cleaning rules step by step
- Joined datasets to create curated Gold table
- Saved everything as Delta tables

Results:
- Cleaned dataset ready for analysis
- All data quality issues fixed
- Gold table with features for ML/analytics