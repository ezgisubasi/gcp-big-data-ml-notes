# Big Data and ML On Google Cloud

![image.png](images/Big%20Data%20and%20ML%20On%20Google%20Cloud/image.png)

- **Big Data & ML Product** (to perform tasks to ingest, store, process and deliver business insights, data pipelines and ML models)
- **Compute and Storage** (seperately because they can scale independently based on need)
- **Network & Security**

# Compute

![image.png](images/Big%20Data%20and%20ML%20On%20Google%20Cloud/image%201.png)

Organizations with growing data needs often require lots of computing power to run Big Data jobs.  

## Computing Services

![image.png](images/Big%20Data%20and%20ML%20On%20Google%20Cloud/image%202.png)

### 1. Compute Engine

- IaaS offering (Infrastructure as a service) provides compute, storage, network resources virtually that are similar to physical data centers.
- individual virtual machine.

### 2. Google Kubernetes Engine - GKE

- GKE runs containerized applications in a cloud environment.
- its not individual

### 3. App Engine

- Fully managed PaaS offering (platform as a service)
- Bind code to libraries that provide access to the infrastructure application needs
- Focused on application logic

### 4. Cloud Functions

- Executes code in response to events (like a new file uploaded to storage)
- Functions as a service offering

### 5. Cloud Run

- Fully managed platform enables you to run requests or event-driven stateless workloads without having to worry about servers.
- Lets you focus on writing code
- Automatically scales up and down (you don’t have to worry about configuration)
- Charges you only for the resources you use

# Storage

![image.png](images/Big%20Data%20and%20ML%20On%20Google%20Cloud/image%203.png)

With cloud computing, processing limitations aren’t attached to storage disks. 

Ex: You can install and run database on a virtual machine using Compute Engine, just like data centers

![image.png](images/Big%20Data%20and%20ML%20On%20Google%20Cloud/image%204.png)

### 1. Cloud Storage 2. Bigtable 3. Cloud SQL 4. Spanner 5. Firestore 6. BigQuery

- The goal of these products is to reduce the time and effort needed to store data. This means creating an Elastic Storage Bucket directly in a web interface or thorugh a command line.

Ex: Cloud Storage; Google cloud offers relational and non-relational databases and worldwide object storage. 

- Choosing the right option to store and process data depends on;
    - Data type
    - Business need

### Unstructured vs Structured Data

![image.png](images/Big%20Data%20and%20ML%20On%20Google%20Cloud/image%205.png)

### 1. Unstructured Data

- Information stored in a non-tabular form such as documents, images, audio files
- Cloud Storage, BigQuery used to store
- **Cloud Storage**
    - Stores objects in containers called buckets
    - All buckets are associated with a project and you can group your projects under an organization
    - Each project, bucket and object in GC is a resource in GC
    - Create project → Create Cloud Storage buckets → Upload objects to your buckets → Download objects from your buckets
    
    Has 4 primary storage classes;
    
    - Standard Storage: Best for frequently accessed or “hot” data and great for data that is stored for only brief periods of time
    - Nearline Storage: Best for infrequently accessed data, like reading or modifying data one per month or less
    - Coldline Storage: Once every 90 days
    - Archive Storage: Once a year (lowest cost option)

### 2. Structured Data

- Represents data stored in tables, rows and columns.
    - **Transactional workloads vs. Analytical workloads**
    You need to choose between SQL and NoSQL options, too. There are compute options for each of them.
    - **Transactional Workloads:
    - Online Transaction Processing Systems:** used when fast data inserts and updates are required to build row-based records. Standardized queries that impact only a few records.
    - **Analytical Workloads:
    - Online Analytical Processing Systems:** used when entire datasets need to be read. Complex queries like aggregations.