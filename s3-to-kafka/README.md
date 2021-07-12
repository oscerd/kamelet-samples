# S3 to Kafka

- Use the quickstart for https://strimzi.io/quickstarts/ and follow the minikube guide.

- Install camel-k on the kafka namespace

- Set the correct credentials for S3 in the flow-binding.yaml

- Run the following commands

kubectl apply -f flow-binding.yaml -n kafka

- Check logs

kamel logs s3-to-kafka -n kafka
