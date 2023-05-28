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
 
