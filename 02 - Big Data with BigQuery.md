# Big Data with BigQuery

BigQuery is a full-managed data warehouse (dw is a large store, contains with a wide range of sources)

### Difference between Data Warehouse vs Data Lake

- Data lake is just a pool of raw, unorganized and unclassified data, which has no specified purpose.
- Data warehouse contains structured and organized data, which can be used for advanced querying.
- A place to store petabytes of data
- A place to analyze data (ml, geospatial, business intelligence)
- Serverless solution, you can only focus SQL queries
- Data encryption at rest by default (you don’t need to do extra anything)
- Has built-in machine learning features, you can write ml models directly in BigQuery using SQL

![image.png](images/Big%20Data%20with%20BigQuery/image.png)

# Storage and Analytics

- Both are connected to Google’s high-speed network, allowing storage and computing to be performed independently as needed.
- Internal data, External data, Multi-cloud data (AWS or Azure), and Public datasets are ingested from multiple sources.
- Offers to query external data sources (cloud storage services) such as Cloud Storage, Cloud Spanner, and Cloud SQL (CSV files)
- For streaming data, you can use Dataflow

### Load data into BigQuery

- Batch load (can be one time or automated to occur on a schedule)
    - Can create a new table or append data to an existing table
- Streaming
    - Smaller batches of data are streamed continuously so that the data is available for querying in near-real time
- Generated data
    - SQL statements are used to insert rows into an existing table or to write the results of a query to a table

### Analyze data

- Ad-hoc Analysis
- Geospatial Analytics
- Building Machine Learning Models
- Building BI Dashboards

# Introduction to BigQuery ML

1. Export data from your datastore into an IDE (integrated development environment)
2. Transform the data and perform feature engineering
3. Build the model in TensorFlow (or similar library) and train it locally or on a virtual machine
4. To improve model performance, you need to get more data and create new features
- You can create and execute machine learning models on your structured datasets in BigQuery using SQL Queries

![image.png](images/Big%20Data%20with%20BigQuery/image%201.png)

![image.png](images/Big%20Data%20with%20BigQuery/image%202.png)

- Manually control hyperparameters or
- Automatically tune hyperparameters (default)

### Supervised vs Unsupervised Models

![image.png](images/Big%20Data%20with%20BigQuery/image%203.png)

### Classification

- Logistic Regression
- DNN Classifier (TensorFlow)
- XGBoost
- AutoML Tables
- Wide and Deep NNs

### Regression

- Linear Regression
- DNN Regressor (TensorFlow)
- XGBoost
- AutoML Tables
- Wide and Deep NNs

### Other Models

- K-means Clustering
- Time Series Forecasting (ARIMA+)
- Recommendation: Matrix Factorization
- Anomally Detection

### ML Ops

- Importing TensorFlow models for batch prediction
- Exporting models from BigQuery ML for online prediction
- Hyperparameter tuning using Vertex AI Vizier

# Using BigQuery ML to predict customer lifetime value (LTV)

## LTV (Lifetime value)

- Used to estimate how revenue or profit you can expect from a **customer given their history** and **customers with similar patterns**
- Goal is to identify **high-value customers** and bring them with special promotions and incentives (rewards, benefits, motivations etc)
- Ex: Customer LTV pageviews, Total visit, Average time spent on the site, total revenue and transactions on the site.

### Feature Engineering in BigQuery ML

- Automatically one-hot encoding categorical values
- Automatically splits the dataset into training data and evaluation data
- If we train a model on the known historical data, and are happy with the performance, we can use it to predict future datasets

# BigQuery ML Project Phases

### Key Phases of ML Project

1. Extract, transform and load data into BigQuery (ETL)
    - If you’e already using other Google products, look out for easy connectors to get that data into BigQuery before you build your own pipeline
    - You can enrich your existing data warehouse with other data sources by using SQL joins
2. Select and preporcess features
    - Use SQL to create the training dataset for the model to learn from
    - BigQuery ML does some of the preprocesing for you, like one-hot encoding of your categorical variables
3. Create the model inside BigQuery
    - 
    
    ![image.png](images/Big%20Data%20with%20BigQuery/image%204.png)
    
4. Evaluate the performance of the trained model
- 

![image.png](images/Big%20Data%20with%20BigQuery/image%205.png)

1. Use the model to make predictions
- 

![image.png](images/Big%20Data%20with%20BigQuery/image%206.png)

# BigQuery ML Key Commands

1. 

![image.png](images/Big%20Data%20with%20BigQuery/image%207.png)

1. 

![image.png](images/Big%20Data%20with%20BigQuery/image%208.png)

- Output of ML.WEIGHTS is numerical value. Each feature has a weight from -1 to 1.
- It shows how **important the feature is for predicting result or label.**
- **Closer to 0** ⇒ the **less important** the feature is to the prediction
- **Closer to -1 or 1** ⇒ the **more important** the feature is to the prediction
1. 

![image.png](images/Big%20Data%20with%20BigQuery/image%209.png)

- You’ll get different performance metrics depending on the model type you choose
1. 

![image.png](images/Big%20Data%20with%20BigQuery/image%2010.png)

## BigQuery ML Commands for Supervised Models

![image.png](images/Big%20Data%20with%20BigQuery/image%2011.png)