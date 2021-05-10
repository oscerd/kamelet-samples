# Kafka to LOG with value to key

- Use the quickstart for https://strimzi.io/quickstarts/ and follow the minikube guide.

- Install camel-k on the kafka namespace

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml -n kafka
kubectl apply -f kafka-not-secured-source.kamelet.yaml -n kafka
kubectl apply -f json-deserialize-action.kamelet.yaml -n kafka
kubectl apply -f json-serialize-action.kamelet.yaml -n kafka
kubectl apply -f value-to-key-action.kamelet.yaml -n kafka
kubectl apply -f flow-binding.yaml -n kafka

- Check logs

kamel logs kafka-to-log-with-value-to-key -n kafka
