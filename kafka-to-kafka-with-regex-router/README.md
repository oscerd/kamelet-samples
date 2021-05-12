# Kafka to Kafka with Regex Router

- Use the quickstart for https://strimzi.io/quickstarts/ and follow the minikube guide.

- Install camel-k on the kafka namespalce

- Set the correct auth token and chat id for the telegram sink kamelet in flow-binding file.

- Run the following commands

kubectl apply -f kafka-not-secured-source.kamelet.yaml -n kafka
kubectl apply -f log-sink.kamelet.yaml -n kafka
kubectl apply -f kafka-not-secured-sink.kamelet.yaml -n kafka
kubectl apply -f regex-router-action.kamelet.yaml -n kafka

- Check logs

kamel logs kafka-to-kafka-with-regex-router -n kafka
