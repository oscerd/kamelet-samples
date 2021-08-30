# Kamelet Samples

A collection of Kamelet Samples

Needed:
- Latest Minikube
- Kamel 1.4.0

- Clone camel-k repository

Spin up a minikube cluster
- minikube start

Set up registry
- minikube addons enable registry

Install camel-k on minikube
- kamel install

Check if everything is working fine
- kubectl get ip

Run samples

## Samples list

- AWS DDB Streams to Telegram
- AWS Kinesis to Log
- AWS S3 to Log
- AWS S3 to Log with Secret
- AWS S3 to Kafka with timestamp router action
- AWS S3 to Kafka
- Azure Storage Blob to Log
- Bitcoin to Log
- Bitcoin to Kafka
- Bitcoin to S3
- FHIR to Telegram
- Secured HTTP to Log
- Kafka to Kafka with regex router action
- Kafka to Kafka with timestamp router action
- Kafka to Log
- Kafka to Log with value to key action
- Kafka to Log with manual commit and Telegram sink
- Kafka to AWS Translate and template to log sink
- Kafka to AWS S3 Streaming Upload Sink
- MongoDB to Log
- PostgreSQL to Log
- Simulation source to AWS Kinesis Firehose
- Simulation source to AWS SNS
- Simulation source to AWS SQS
- Simulation source to AWS SQS FIFO
- Simulation source to AWS Translate to Log
- Simulation source to Azure Storage Blob
- Simulation source to Dropbox
- Simulation source to Kafka
- Simulation source to Kafka with message timestamp router action
- Simulation source to Log with extract field action
- Simulation source to Log with hoist field action
- Simulation source to Log with insert field action
- Simulation source to Log with insert header action
- Simulation source to Log with mask field action
- Simulation source to Log with replace field action
- Simulation source to Log with predicate filter action
- Simulation source to Log with Mustache template action
- Simulation source to Log with Json Schema Validator action
- Simulation source to Log with Jsonata action
- Simulation source to Log with XJ Identity action
- Simulation source to AWS S3
- Simulation source to MongoDB
- Simulation source to MS SQL Server
- Time-based HTTP Invocation invocation to Log
- Time-based HTTP Invocation invocation to Kafka
- Time-based EC2 status invocation to Log
- Time-based Lambda invocation to Telegram
- Time-based to S3 Streaming Upload Sink
- Time-based to Log with Has Header Filter
- Time-based to Log with Tombstone Filter
- Time-based to Log with Topic Name Matches Filter

