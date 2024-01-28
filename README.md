End to End On-Prem SQL Database Migration to Azure cloud Project.

Objective: 
The primary objective of this project is to execute a seamless migration of an existing On-Premises SQL Server database to the Azure Cloud while strategically integrating advanced analytics capabilities. By doing so, we aim to enhance data accessibility, scalability, and analytical potential, enabling our organization to harness the full power of Azure's cloud infrastructure for informed decision-making and strategic insights.

Azure SQL Database Migration and Analytics Architecture:

Components:

1.	On-Premises SQL Server Database:
•	The existing SQL Server database containing Bike Spare Part sales data.

2.	Azure Self-Host Integration Runtime:
•	Used to migrate the data from the On-Premises SQL Server to Azure SQL Database.

3.	Azure SQL Database:
•	The target database in the Azure Cloud where the On-Premises data will be migrated.

4.	Azure Databricks:
•	Utilized for data transformation, cleaning, and analytics processing.
•	Databricks clusters running notebooks for ETL (Extract, Transform, Load) processes.

5.	Azure Storage Datalake Gen2:
•	Storage for intermediate and raw data, providing a scalable and cost-effective solution.
•	Staging area for data before it is transformed by Databricks.

6.	Azure Synapse Studio:
•	Functions as a comprehensive analytics and data warehousing solution.
•	Stores cleaned and transformed data for advanced analytics.

7.	Power BI:
•	Visualization tool for creating reports and dashboards.
•	Direct connection to Azure SQL Database for real-time reporting.



DATASET:




