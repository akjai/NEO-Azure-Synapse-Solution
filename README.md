# NEO-Azure-Synapse-Solution

This is an end-to-end Data & AI solution in Azure that predicts the threat level of Near Earth Objects (NEO). Services used: Azure Cosmos DB, Azure Data Lake Storage Gen2, Azure Synapse Analytics, Azure Machine Learning.

Synapse pipelines are used to ingest, clean, and transform the original dataset (found here: https://www.kaggle.com/datasets/sameepvani/nasa-nearest-earth-objects) into tables ready for data warehousing. 

Azure Data Lake Storage Gen2 stores the data at different landing zones. 

Azure ML is used to train a model on this dataset to predict the threat level of NEOs. 

Cosmos DB is used as a transactional store for incoming unclassified NEO data. This data is ingested, cleaned, and then passed through the trained ML model to classify the hazardous level of each NEO as 'true' or 'false'. 

PPT with architecture diagram and Data Lake landing zone explanations: https://microsoft-my.sharepoint.com/:p:/p/t-jainankit/EQU0AlCwTldDr9--RVZHqT0Bvs6TzWt4FTXKWdb6TAN1fA?e=bkw3XT
