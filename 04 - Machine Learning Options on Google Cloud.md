# Machine Learning Options on Google Cloud

# Options to build ML models

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image.png)

### 1. BigQuery ML

- Use SQL queries to create and execute machine learning models in BigQuery
- If you already have your data in BigQuery and your problems fit the pre-defined ML models, this could be your choice
- Data type: Tabular
- Training data size: Medium to large
- ML and coding expertise: Medium
- Flexibility to tune hyperparameters: Medium
- Time to train a model: Medium

### 2. Pre-built APIs

- Leverage ML models that have already ben built and trained by Google
- You don’t have to build your own machine learning models if you don’t have enough training data or sufficient ML expertise
- Data Type: Tabular, image, text, and video
- Training data size: No data required
- ML and coding expertise: Low
- Flexibility to tune hyperparameters: None
- Time to train a model: None

### 3. AutoML

- A no-code solution to build ML models on Vertex AI
- Data Type: Tabular, image, text, and video
- Training data size: Small to medium
- ML and coding expertise: Low
- Flexibility to tune hyperparameters: None
- Time to train a model: Medium

### 4. Custom Training

- Code your own ML environment to have control over the ML pipeline
- Gives you flexibility
- Data type: Tabular, image, text, and video
- Training data size: Medium to large
- ML and coding expertise: High
- Flexibility to tune hyperparameters: High
- Time to train a model: Long

# Pre-built APIs

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image%201.png)

### 1. Speech-to-Text API

- Convert audio to text for data processing

### 2. Cloud Natural Language API

- Recognizes parts of speech called entities and sentiment

### 3. Cloud Translation API

- Converts text from one language to another

### 4. Text-to-Speech API

- Converts text into high-quality voice audio

### 5. Vision API

- Works with and recognizes static images

### 6. Video Intelligence API

- Recognizes motion and action in video

# Auto ML (Automated machine learning)

Automates machine learning pipelines to save data scientists from manual work 

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image%202.png)

## Transfer Learning

Transfer learning is a powerful technique that lets people with smaller datasets, or less computational power, achieve state-of-art results by taking advantage of pre-trained models that have been trained of similar but larger datasets.

- It can reach higher accuracy with much less data and computation time

## Neural Architecture Search

The goal of the neural architecture search is to find the optimal model for the relevant project.

- Powered by the latest ML research
- Trains and evaluates multiple models
- Produces an ensemble of ML models
- Chooses the **best** one

Train custom ML models with

- Minimal effort
- Little machine learning expertise

Allows data scientists to focus on

- Defining business problems
- Evaluating and improving model results

### How does it work?

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image%203.png)

Supports four types of data: Image, Tabular, Text, Video

- AutoML solves different types of problems called **objectives**
- Upload your data to AutoML (from Cloud Storage, BigQuery, or a local machine)
- **Image data**:
    - Use a **classification model** to analyze image data and return a list of content categories that apply to the image
    - Use an **object detection model** to analyze your image data and return annotations that consist of a label and bounding box location for each object found in an image
- **Tabular data:**
    - Use a **regression model** to analyze tabular data and return a numeric value
    - Use a **classification model** to analyze tabular data and return a list of categories
    - A f**orecasting model** can use multiple rows of time-dependent tabular data from the past to predict a series of numeric values in the future
- **Text data:**
    - Use a **classification model** to analyze text data and return a list of categories that apply to the text found in the data
    - An **entity extraction model** can be used to inspect text data for known entities referenced in the data and label those entities in the text
    - A **sentiment analysis model** can be used to inspect text data and indentify the prevailing emotional opinion within it (positive, negative or neutral comments)
- **Video data:**
    - Use a **classification model** to analyze video data and return a list of categorized shots and segments
    - Use an **object tracking model** to analyze video data and return a list of shots and segments where these objects were detected
    - An **action recognition model** can be used to analyze video data and return a list of categorized actions, along with the moments when the actions happened

# Custom Training

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image%204.png)

Code your own ML environment to have full control over the entire process

- **Vertex AI Workbench** is a single development environment for the entire data science workflow from exploring to training and then deploying a machine learning model with code
- Pre-built Container: when you need libraries such as
    - Tensorflow, Pytorch, Scikit-learn, XGBoost, Python code
- Custom Container:
    - You define the exact tools that you need to complete the job

# Vertex AI

Create → Deploy → Manage

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image%205.png)

### Data readiness

- Users can upload data from wherever it’s stored; Cloud Storage, Big Query or a local machine

### Feature readiness

- Users can create features, which are the processed data that will be put into the model, and then share them with others using the feature store

### Training and hyperparameter tuning

- When the data is ready, users can experiment with different models and adjust hyperparameters

### Deployment and model monitoring

- Users can set up the pipeline to transform the model into production by automatically monitoring and performing continuous improvements

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image%206.png)

# AI Solutions

![image.png](images/Machine%20Learning%20Options%20on%20Google%20Cloud/image%207.png)