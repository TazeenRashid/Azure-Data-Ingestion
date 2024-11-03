<h1>Automated Data Ingestion Pipeline from On-Premises SQL Server to Azure Data Lake Storage Gen2</h2>

This project demonstrates an end-to-end automated data ingestion pipeline designed to ingest, secure, and synchronize data from an on-premises SQL Server into Azure Data Lake Storage Gen2 (ADLS Gen2). The solution includes automated updates, secure credential management with Azure Key Vault, and data stored in Parquet format for optimized analytics.

<b>Project Overview</b>
The primary goal of this project is to automate the ingestion of on-premises data into a cloud environment, ensuring it’s accessible for further transformation and visualization. By using Azure Data Factory (ADF) for orchestration and Azure Key Vault for secure credential management, this pipeline enables real-time updates and data synchronization, eliminating the need for manual intervention.

<b>Project Steps</b>

<b>1. Setting Up the Azure Resources</b>
Resource Group Creation: First, I created a resource group in Azure to organize all relevant resources (Data Factory, Storage Account, Key Vault).
Storage Account Creation: I set up a Storage Account with a container for ADLS Gen2, which will store the ingested data in Parquet format. Parquet was chosen for its efficient storage and performance benefits, especially for analytical workloads.

<b>2. Azure Data Factory (ADF) Pipeline Configuration</b>
Pipeline Creation: Using Azure Data Factory, I designed a pipeline to orchestrate the movement of data from SQL Server to ADLS Gen2.
Linked Services Configuration: I set up linked services in ADF to securely connect to both the SQL Server (source) and the ADLS Gen2 (destination).
Integration of Key Vault for Security: To manage sensitive credentials (like database access keys) securely, I integrated Azure Key Vault into ADF. This integration allows ADF to retrieve secrets directly from Key Vault without hardcoding any credentials in the pipeline.

<b>3. Data Pipeline Details</b>
Data Movement Activities: The ADF pipeline includes activities to move data from the on-premises SQL Server to ADLS Gen2.
Transformation Options: Although no transformation was applied in this initial ingestion phase, the pipeline can be easily modified to include data transformations in future iterations.
Scheduling and Triggering: I configured the pipeline to run on a schedule, ensuring regular data updates. This setup also supports real-time ingestion through triggers, so any change in the SQL Server data can automatically update the data lake.

<b>4. Automated Data Synchronization with Real-Time Updates</b>
Automation Setup: The pipeline is automated to detect changes in the SQL Server and trigger a data update in ADLS Gen2.
Real-Time Syncing: This automation ensures that whenever data changes on-premises, it’s automatically updated in the cloud. As a result, the cloud data is always in sync with the source without requiring any manual intervention.

<b>5. Data Security with Azure Key Vault</b>
Storing Secrets in Key Vault: All sensitive credentials, such as database passwords and storage account keys, are stored in Azure Key Vault, enhancing security by avoiding hardcoded credentials in the pipeline.
Access Management: ADF retrieves these credentials as needed during the pipeline execution, ensuring secure access and reducing the risk of exposing sensitive information.

<b>6. Data Storage in ADLS Gen2 in Parquet Format</b>
Efficient Storage for Analytics: Once the data reaches ADLS Gen2, it’s stored in Parquet format. Parquet is columnar and optimized for analytical processing, which makes it an excellent choice for data transformations and queries.
Readiness for Further Processing: The ingested data is now available in the cloud and ready for further transformation and analysis using tools like Azure Databricks and Azure Synapse Analytics.

<b>7. Transformation & Visualization Options</b>
Data Transformation with Azure Databricks or Synapse Analytics: From this point, the data can be transformed as per business requirements in Azure Databricks or Synapse Analytics, creating ready-to-use data for reporting.
Visualization with Power BI and Tableau: Finally, the data in ADLS can be directly connected to Power BI or Tableau for visualization, making the data accessible for business decision-making with up-to-date insights.

<b>Key Features of the Project</b>

<b> <li> End-to-End Automation:</b> The pipeline automates the ingestion of data from on-premises SQL Server to Azure Data Lake Storage, including automated updates for real-time synchronization. </li> 
<b> <li>Enhanced Security with Key Vault:</b> All credentials are securely managed in Azure Key Vault, preventing exposure of sensitive data and allowing for secure pipeline execution. </li> 
<b> <li>Optimized Storage with Parquet Format:</b> Data is stored in Parquet format, enabling efficient storage and retrieval for analytical workloads. </li> 
<b> <li>Transformation & Visualization-Ready Data: </b> The ingested data is accessible for transformation in Azure Databricks or Synapse Analytics and can be visualized in Power BI or Tableau for business insights.</li> 

<b> Tech Stack</b> 
<li>Azure Data Factory - For data orchestration and pipeline creation.</li>
<li>Azure Data Lake Storage Gen2 - For cloud-based, scalable data storage.</li>
<li>Azure Key Vault - For secure credential management.</li>
<li>On-premises SQL Server - Data source for the project.</li>
<li>Power BI / Tableau - For data visualization and business reporting.</li>
<li>Skills & Tools Highlighted </li>
<li>Data ingestion & pipeline creation with ADF </li>
<li>Secure credential management with Azure Key Vault </li>
<li>Automated data synchronization </li>
<li>Cloud storage and data processing with ADLS Gen2 </li>
<li>Real-time data accessibility for visualization and reporting </li>
