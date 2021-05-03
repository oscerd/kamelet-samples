# Kafka to LOG 

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs kafka-to-log
