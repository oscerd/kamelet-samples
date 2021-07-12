# S3 to Kafka with Timestamp Router

- Use the quickstart for https://strimzi.io/quickstarts/ and follow the minikube guide.

- Install camel-k on the kafka namespalce

- Set the correct credentials for S3 in the flow-binding.yaml

- Run the following commands

kubectl apply -f kafka-not-secured-source.kamelet.yaml -n kafka
kubectl apply -f log-sink.kamelet.yaml -n kafka
kubectl apply -f kafka-not-secured-sink.kamelet.yaml -n kafka
kubectl apply -f timestamp-router-action.kamelet.yaml -n kafka
kubectl apply -f flow-binding.yaml -n kafka

- Check logs

kamel logs s3-to-kafka-with-timestamp-router -n kafka
