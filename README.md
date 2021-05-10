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
- FHIR to Telegram
- Kafka to Log
- Kafka to Log with value to key action
- Simulation source to AWS Kinesis Firehose
- Simulation source to AWS SNS
- Simulation source to AWS SQS
- Simulation source to AWS SQS FIFO
- Simulation source to Azure Storage Blob
- Simulation source to Dropbox
- Simulation source to Kafka
- Simulation source to Log with extract field action
- Simulation source to Log with hoist field action
- Simulation source to Log with insert field action
- Simulation source to Log with insert header action
- Simulation source to Log with mask field action
- Simulation source to Log with replace field action
- Time-based Lambda invocation to Telegram

