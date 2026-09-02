# AWS + Snowflake + Power BI Agriculture Analytics Project

This project demonstrates a complete end-to-end data analytics workflow using an agricultural dataset stored in AWS, loaded into Snowflake, and visualized in Power BI. The objective was to bring raw CSV data from cloud storage into a modern warehouse, clean and enrich it, and then build meaningful business intelligence dashboards for analysis.

## Project Overview

The dataset used in this project contains agricultural and seasonal information such as:

- Year
- Location
- Area under cultivation
- Rainfall
- Temperature
- Soil Type
- Irrigation Method
- Yield
- Humidity
- Crop Type
- Price
- Season

The project focuses on understanding how crop performance and agricultural output vary across regions, seasons, and environmental conditions.

## Business Goal

The main goal of this project was to:

- Import the CSV dataset from AWS storage into Snowflake
- Create a warehouse-ready data model for analysis
- Transform and enrich the raw data using SQL
- Build a Power BI dashboard to visualize trends and patterns
- Support decision-making related to agriculture, rainfall, crop performance, and regional productivity

## Architecture

The data pipeline follows this flow:

1. CSV file stored in AWS S3
2. Snowflake storage integration configured to access AWS S3
3. Raw data loaded into Snowflake tables
4. SQL transformations applied for data preparation
5. Snowflake connected to Power BI
6. Dashboards and visualizations created in Power BI

## Tech Stack

- AWS S3: source storage for the CSV file
- Snowflake: data warehouse and transformation layer
- SQL: for data loading, cleaning, and enrichment
- Power BI: dashboard creation and reporting
- CSV dataset: agricultural data source

## Project Files

- `data-season.csv` — raw agricultural dataset used for this project
- `snowflake.sql` — SQL script for Snowflake setup, staging, loading, and transformation
- `README.md` — project documentation

## Data Workflow

### 1. AWS to Snowflake

The CSV file was first uploaded to an AWS S3 bucket. A Snowflake storage integration object was created so Snowflake could securely access the S3 location. A Snowflake stage was then created to reference the data in S3.

### 2. Data Loading into Snowflake

The raw CSV file was loaded into a Snowflake table using the COPY INTO command. The file format was defined with comma-separated values and a header row was skipped during import.

### 3. Data Transformation

After loading, several SQL operations were performed, including:

- Creating normalized tables and staging structures
- Applying business logic for year grouping
- Categorizing rainfall into Low, Medium, and High groups
- Updating agricultural data for analysis
- Preparing a cleaned dataset for reporting

### 4. Power BI Connection

Once the data was available in Snowflake, it was connected to Power BI. The project then used Power BI to create visual reports and dashboards for:

- Crop trends by year
- Regional comparison
- Seasonal analysis
- Rainfall and yield relationships
- Crop price and productivity insights

## Key Data Dimensions

The dataset allows analysis across several important dimensions:

- Year and year group
- Geographic location
- Crop type
- Soil type
- Irrigation method
- Rainfall category
- Season
- Yield and price

## Example Business Questions Addressed

This dashboard can help answer questions like:

- Which regions have the highest agricultural productivity?
- How do rainfall levels impact crop yield?
- Which crops generate the most value?
- How do seasonal patterns affect agricultural output?
- What is the relationship between irrigation and yield?

## SQL Highlights

The Snowflake script includes operations such as:

- Storage integration setup
- Database and schema creation
- Table creation
- Stage creation
- COPY INTO for loading the CSV
- Data updates for analytical grouping
- Rainfall classification logic
- Year segmentation for reporting

## Visualization Outcome

The Power BI dashboard created from this data helps stakeholders understand agricultural performance visually and make data-driven decisions based on historical trends and environmental factors.

## How to Use This Project

1. Upload the CSV file to your AWS S3 bucket.
2. Use the Snowflake SQL script in `snowflake.sql` to configure the integration, stage, and tables.
3. Run the provided SQL commands to load the dataset.
4. Connect Snowflake to Power BI.
5. Build visualizations using the transformed agricultural dataset.

## Notes

This project is a good example of a real-world cloud data pipeline where raw business data moves from storage to a cloud warehouse and then into a reporting layer. It combines data engineering and business intelligence practices in a single workflow.

## Conclusion

This project showcases how cloud storage, warehouse processing, and visualization tools can be integrated to turn raw agricultural data into actionable insights. It demonstrates a practical analytics workflow from AWS to Snowflake to Power BI, which is highly relevant for modern data-driven business environments.

## Future Improvements

Potential enhancements for this project include:

- Adding automated ETL pipelines
- Building a more polished Power BI dashboard design
- Incorporating forecasting and trend analysis
- Extending the dataset with additional agriculture metrics
- Creating scheduled refresh and reporting automation

