# Kafka to AWS Translate with template to Log

- Use the quickstart for https://strimzi.io/quickstarts/ and follow the minikube guide.

- Install camel-k on the kafka namespace

- Set correctly the AWS Credentials for AWS translate in the flow-binding file

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

Ingest data in your kafka topic

- Check logs

kamel logs kafka-translate-template-to-log
