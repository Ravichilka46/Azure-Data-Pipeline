End to End On-Prem SQL Database Migration to Azure cloud Project.

Objective: 
The primary objective of this project is to execute a seamless migration of an existing On-Premises SQL Server database to the Azure Cloud while strategically integrating advanced analytics capabilities. By doing so, we aim to enhance data accessibility, scalability, and analytical potential, enabling our organization to harness the full power of Azure's cloud infrastructure for informed decision-making and strategic insights.

Azure SQL Database Migration and Analytics Architecture:


Components:


1.	On-Premises SQL Server Database:

The existing SQL Server database containing Bike Spare Part sales data.

2.	Azure Self-Host Integration Runtime:

Used to migrate the data from the On-Premises SQL Server to Azure SQL Database.

3.	Azure SQL Database:

The target database in the Azure Cloud where the On-Premises data will be migrated.

4.	Azure Databricks:

Utilized for data transformation, cleaning, and analytics processing.
Databricks clusters running notebooks for ETL (Extract, Transform, Load) processes.

5.	Azure Storage Datalake Gen2:

Storage for intermediate and raw data, providing a scalable and cost-effective solution.
Staging area for data before it is transformed by Databricks.

6.	Azure Synapse Studio:

Functions as a comprehensive analytics and data warehousing solution.
Stores cleaned and transformed data for advanced analytics.

7.	Power BI:

Visualization tool for creating reports and dashboards.
Direct connection to Azure SQL Database for real-time reporting.



DATASET:  AdventureAdventureWorksLT2017.bak


https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms



1) On-Prem SQL Server Setup:

![On prem SQL Server Tables](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/33046d79-46e9-43cc-9bbf-60ee647f0cb3)


2) Azure Cloud Resource Group:

Configured Azure Datalake gen2, Azure Databricks workspace, Azure Data Factory, Azure Sql Server, Azure Key Vault, Azure Synapse Studio

![Azure Resource Group](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/1828b9f1-ad30-4b01-a4d2-48154a8b9c75)

3) Firewall settings and Role Access Settings:

![Role Access](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/86a659fa-7b0d-455f-8e64-552bcf95274e)

4) Azure Databricks Transformation:

Change Date column type from DateTime to Timestamp

![Azure Databricks Silver](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/94a99961-b4e3-41ef-a4b3-1f03926ebc33)


Change Column names: 

![Azure Databricks](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/6b8c02b2-a3f1-4a79-be8f-b0cceb9b3185)



5) Azure Data Factory Pipeline:


Pipeline Imports data in Bronze container and does 1st level transformation in Silver container and Final cleaned data storage in Gold conatainer

![ADF activity](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/0a87cdfa-7c2c-4da6-a6a0-5338435bc4d1)


6) Azure Synapse Analystics:


The Transformed Data is Migrated to Synapse Anayltics Sql Server DB and runs on Serverless Sql Pool.

![Azure Synapse Analytics](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/bc936a43-a356-4c2f-bb38-948f5d97b01a)


7) POWER BI Data Modeling and Dashboard:



![Data Modelling](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/2b2d2ea1-a7ba-474c-95c5-dfcaa007e569)


![Power BI Report](https://github.com/Ravichilka46/Azure-Data-Pipeline/assets/67186516/935cb3ed-dcec-4953-bffd-25b0b4ddfb65)

