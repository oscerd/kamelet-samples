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

Use the minikube docker env
- eval $(minikube docker-env)

Build camel k
- make images

Install camel-k on minikube
- ./kamel install

Check if everything is working fine
- kubectl get ip

Run samples

## Samples list

- AWS DDB Streams to Telegram
- FHIR to Telegram
- Simulation source to AWS Kinesis Firehose
- Simulation source to AWS SNS
- Simulation source to AWS SQS
- Simulation source to AWS SQS FIFO
- Simulation source to Azure Storage Blob
- Simulation source to Dropbox
- Simulation source to Log with insert header action
- Time-based Lambda invocation to Telegram

