# NYC Payroll Data Integration Project

##  Overview

This project demonstrates a full data integration pipeline using **Azure Data Factory**, **Azure Data Lake Storage Gen2**, **Azure SQL Database**, and **Azure Synapse Analytics**. The pipeline ingests NYC Payroll data (2021 and historical), transforms it, and loads it into Synapse Analytics for advanced analytics and reporting.


##  Objectives

- Load and transform 2021 payroll data from Azure Data Lake into Azure SQL Database.
- Load historical payroll data from Azure Data Lake.
- Merge and aggregate all data (current + historical).
- Load final datasets into Azure Synapse Analytics.
- Create orchestrated pipelines and parameterized dataflows.
- Integrate project with GitHub for source control.


##  Architecture

- **Source**: CSV files stored in Azure Data Lake Gen2
- **Staging**: Azure SQL Database (for 2021 data)
- **Analytics**: Azure Synapse Analytics (for final reporting)
- **Orchestration**: Azure Data Factory
- **Version Control**: GitHub Integration



##  Key Components

### 🔗 Linked Services
- Azure Data Lake Gen2
- Azure SQL Database
- Azure Synapse Analytics

###  Datasets
- `nycpayroll_2021.csv`
- `EmpMaster.csv`
- `TitleMaster.csv`
- `AgencyMaster.csv`
- Destination datasets in SQL DB and Synapse tables

###  Dataflows
- Load 2021 payroll to SQL DB
- Load historical data from lake
- Aggregate & transform payroll data
- Load Employee, Title, and Agency master data
- Load data from SQL DB to Synapse

###  Pipelines
- Individual pipelines for each dataflow
- Master pipeline to run all flows in sequence or parallel

##  Output Tables (in Synapse Analytics)

| Table Name                    | Description                            |
|------------------------------|----------------------------------------|
| NYC_Payroll_Data             | Merged payroll data (2021 + history)   |
| NYC_Payroll_EMP_MD           | Employee master data                   |
| NYC_Payroll_TITLE_MD         | Job title master data                  |
| NYC_Payroll_AGENCY_MD        | Agency master data                     |
| NYC_Payroll_Summary          | Aggregated report by Agency & Year     |



##  Steps to Reproduce

1. Set up Linked Services in ADF
2. Create datasets for all sources and targets
3. Build dataflows and add proper mappings
4. Create pipelines to trigger dataflows
5. Add parameters and validation rules
6. Publish to GitHub
7. Run pipelines and verify output in Synapse tables


##  Authentication Notes

Edit the PostgreSQL file with host, user ,and password

