# kafka
streaming data pipeline using kafka
## Project overview 
implemented a streaming data pipeline using Kafka to ingest data from producers and deliver it to consumers. The data is then pushed to Amazon S3, where it is subsequently crawled using the Amazon Glue crawler, enabling the execution of SQL queries on Amazon Athena.
## steps
- Step 1:
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
 ## tools and services used :
 - jupter notebook : to write python code that create the producer and the consumer
 - apache kafka :  is an open-source distributed streaming platform ,  It is designed to handle high-throughput, fault-tolerant, and real-time data streaming applications. 
 - EC2 : a web service provided by Amazon Web Services (AWS) that allows you to provision and manage virtual servers, known as EC2 instances, in the cloud
 - S3 : is a highly scalable and durable cloud storage service provided by Amazon Web Services (AWS). It is designed to store and retrieve large amounts of data, such as files, documents, images, videos, and backups, in a simple and secure manner.
 - IAM :is a web service provided by Amazon Web Services (AWS) that enables you to manage access to AWS resources securely. 
 - - used to create a user so i can use the access key id and secret access key to connect the s3 bucket 
 - - used to create role to allow the glue crawler to access s3
 -  glue crawler : The Glue crawler scans your data sources and automatically creates a metadata catalog, known as the AWS Glue Data Catalog. It extracts information about the structure, schema, and properties of the data, including table definitions, partitions, and the relationships between tables.
 - glue data catalog :The Glue Data Catalog allows you to discover and catalog various data sources, including files stored in Amazon S3, databases, and data warehouses. It automatically extracts metadata about the structure, schema, and properties of the data sources, providing a comprehensive view of your data assets.
 - Amazon Athena :an interactive query service that allows you to analyze data directly from various data sources using standard SQL queries. It is a serverless service, which means you don't need to provision or manage any infrastructure. Athena integrates seamlessly with the AWS Glue Data Catalog to provide a convenient and powerful way to query and analyze the data stored in the Data Catalog.
