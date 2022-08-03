# NEO-Azure-Synapse-Solution

This is an end-to-end Data & AI solution in Azure that predicts the threat level of Near Earth Objects (NEO). Services used: Azure Cosmos DB, Azure Data Lake Storage Gen2, Azure Synapse Analytics, Azure Machine Learning.

Architecture diagram: 
![image](https://user-images.githubusercontent.com/55563026/182654990-5b838df7-5d18-4829-9031-6a68124f7477.png)

Synapse pipelines are used to ingest, clean, and transform the original dataset (found here: https://www.kaggle.com/datasets/sameepvani/nasa-nearest-earth-objects) into data warehouse tables. 

Azure Data Lake Storage Gen2 stores the data at different landing zones:

<img width="838" alt="image" src="https://user-images.githubusercontent.com/55563026/182655085-fffc2113-3530-4479-bdbf-f13d9045d95a.png">

Azure ML is used to train a model on this dataset to predict the threat level of NEOs. 

Cosmos DB is used as a transactional store for incoming unclassified NEO data. This data is ingested, cleaned, and then passed through the trained ML model to classify the hazardous level of each NEO as 'true' or 'false'. 

PPT with architecture diagram and Data Lake landing zone explanations: https://microsoft-my.sharepoint.com/:p:/p/t-jainankit/EQU0AlCwTldDr9--RVZHqT0Bvs6TzWt4FTXKWdb6TAN1fA?e=bkw3XT
