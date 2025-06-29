# Machine Learning Workflow with Vertex AI

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image.png)

### Data Preparation

1. Data uploading
2. Feature Engineering
- Data types
    - Streaming vs batch data
    - Structured vs unstructured data

### Model Training

- A model needs a tremendous amount of iterative training
- Train and evaluate data cycles

### Model Serving

- A model needs actually to be used in order to predict results
- Machine learning models:
    - Deployed
    - Monitored
    - Managed
- If you don’t move an ML model into production, it has no use and remains only a theoretical model
- ML workflow isn’t linear, it’s iterative
    - Ex: During model training, you may need to return to dig into the raw data and generate more useful features to feed the model

### How does Vertex AI support this workflow?

Provides two options for ML models

1. **AutoML:** codeless solution
2. **Custom training:** code-based solution
- **Feature Store:**
    - A centralized repository for organizing, storing and serving features to feed to training models
- **Vizier:**
    - Helps tune hyperparameters in complex machine learning models
- **Explainable AI:**
    - Help interpret training performance and model behaviors
- **Pipelines:**
    - Helps automate and monitor the ML production line

# Data Preparation

(AutoML Workflow)

### 1. Upload Data

- When you upload a dataset in the Vertex AI user interface, you’ll need to provide a **meaningful name** for the data and then select the **data type (image, tabular, text, and video) and objective**.
- Check data requirements
- Add labels to the data if you haven’t already
    - **Label:** It ****is a training target.
        - Can be manually added
        - Can be added by Google’s paid label service via the Vertex console
- Final step is to upload the data (Local source, BigQuery, Cloud Storage)

### 2. Feature Engineering

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image%201.png)

Data must be processed before the model starts training

- A **feature** refers to a factor that contributes to the prediction.
    - Independent variable in statistics
    - Column in a table

### Vertex AI Feature Store

- Function for feature engineering
- A centralized repository to organize, store and serve machine learning features
    - Aggregates all the different features from different sources
    - Updates the features to make them available from a central repository
        - When engineers need to model something, they can use the features available in the Feature Store dictionary to build a dataset

# Model Training

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image%202.png)

### Supervised vs Unsupervised Learning

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image%203.png)

# Model Evaluation

Vertex AI provides extensive evaluation metrics to help determine the performance of the model

- **Evaluation metrics**
    - Confusion matrix
        - Recall
        - Precision
    - Feature Importance

### Confusion Matrix

- A specific performance measurement for machine learninig classification problems
- It’s a table with combinations of predicted and actual values

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image%204.png)

- **True Positive:**
    - The model predicted positive and that’s true
    - Ex: Model predicted this image as cat and it actually is
- **True Negative:**
    - The model predicted negative and that’s true
    - Ex: Model predicted image as not cat and that’s true
- **False Positive (Type 1 Error):**
    - The model predicted positive and that’s false
    - Ex: Model predicted image as cat but that’s not true
- **False Negative (Type 2 Error):**
    - The model predicted negative and that’s not true
    - Ex: Model predicted image as not cat and that’s not true

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image%205.png)

### Recall

- Refers to all the positive cases and looks at how many were predicted correctly ⇒ TP / (TP+FN)

### Precision

- Refers to all the cases predicted as positive and how many are actually positive ⇒ TP / (TP+FP)

### Feature Importance

In Vertex AI, feature importance is displayed through a bar chart to illustrate how each feature contributes to a prediction

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image%206.png)

This information helps decide which features are included in a machine learning model to predict the goal

# Model Deployment and Monitoring

Final step of the machine learning workflow

### Practicing MLOps

![image.png](images/Machine%20Learning%20Workflow%20with%20Vertex%20AI/image%207.png)

Advocating for automation and monitoring at each step of the ML system construction.

- Adopting a process to enable
    - **Continuous integration (CI)**
    - **Continuous training (CT)**
    - **Continuous delivery (CD)**

### 1. Model Deployment

- Endpoint
    - Best when **immediate results** with low latency are needed
        - Ex: Instant recommendations based on a user’s browsing habits whenever they’re online
    - Must be deployed to an endpoint before that model can be used to serve real-time predictions
- Batch prediction
    - Best when **no immediate response is required**, and accumulated data should be processed with a single request
        - Ex: Sending out new ads every other week based on the user’s recent purchasing behavior and what’s currently popular on the market
- Offline prediction
    - Best when the model should be deployed in a specific environment **off the cloud**

### 2. Model Monitoring

- **Vertex AI Pipelines**
    - Automate
    - Monitor
    - Govern (orchestrates workflow in a serverless manner)
- **Vertex AI Workbench**
    - Define your own pipeline with prebuilt pipeline components