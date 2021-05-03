# Kafka to LOG 

- Use the quickstart for https://strimzi.io/quickstarts/

- Install camel-k on the kafka namespalce

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml -n kafka
kubectl apply -f flow-binding.yaml -n kafka

- Check logs

kamel logs kafka-to-log -n kafka
