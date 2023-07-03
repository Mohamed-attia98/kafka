# kafka
streaming data pipeline using kafka
## Project overview 
implemented a streaming data pipeline using Kafka to ingest data from producers and deliver it to consumers. The data is then pushed to Amazon S3, where it is subsequently crawled using the Amazon Glue crawler, enabling the execution of SQL queries on Amazon Athena.
## steps
- _Step 1_:
Installed Kafka on EC2 instance and created a topic to push data through it.
- step 2:
 Wrote a Python script to create a producer that pushed data to the Kafka topic.
- step 3:
 Implemented a Python script to create a consumer that received data from the Kafka topic.
- step 4:
Created an S3 bucket and linked it with the consumer for pushing the data onto it.
- step 5:
Used Amazon Glue Crawler, which automatically scanned and cataloged the metadata of data sources
- step 6:
 Used Glue Data Catalog as the central repository where the metadata collected by the Glue crawler was stored.
- step 7:
 Used Amazon Athena to analyze data directly using standard SQL queries.
 ## Tools and services used:
- Jupyter Notebook: Used to write Python code that creates the producer and the consumer.
- Apache Kafka: An open-source distributed streaming platform designed to handle high-throughput, fault-tolerant, and real-time data streaming applications.
- EC2: A web service provided by Amazon Web Services (AWS) that allows you to provision and manage virtual servers, known as EC2 instances, in the cloud.
- S3: A highly scalable and durable cloud storage service provided by Amazon Web Services (AWS). It is designed to store and retrieve large amounts of data, such as files, documents, images, videos, and backups, in a simple and secure manner.
- IAM: A web service provided by Amazon Web Services (AWS) that enables you to manage access to AWS resources securely. 
  - It is used to create a user so that access key ID and secret access keys can be used to connect to the S3 bucket. 
  - It is also used to create a role to allow the Glue crawler to access S3.
- Glue Crawler: The Glue crawler scans your data sources and automatically creates a metadata catalog known as the AWS Glue Data Catalog. It extracts information about the structure, schema, and properties of the data, including table definitions, partitions, and the relationships between tables.
- Glue Data Catalog: The Glue Data Catalog allows you to discover and catalog various data sources, including files stored in Amazon S3, databases, and data warehouses. It automatically extracts metadata about the structure, schema, and properties of the data sources, providing a comprehensive view of your data assets.
- Amazon Athena: An interactive query service that allows you to analyze data directly from various data sources using standard SQL queries. It is a serverless service, meaning you don't need to provision or manage any infrastructure. Athena seamlessly integrates with the AWS Glue Data Catalog, providing a convenient and powerful way to query and analyze the data stored in the Data Catalog.
## Project life cycle
![kafka project](https://github.com/Mohamed-attia98/ITI-Graduation-Project/assets/82019926/b0ba31cb-08b0-4840-a0ee-6a9f6b40a24e)
## files 
- `indexProcessed.csv `:  file contains the stock market dataset used in the project.
- `kafka-producer.ipynb`:  Python script is used to create the producer, which sends data through the topic.
- `kafka-consumer.ipynb`:  Python script is used to pull data from the topic and push it to an S3 bucket.
