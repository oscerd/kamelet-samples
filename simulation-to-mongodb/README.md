# Simulation to MongoDB

- Using the Camel-K 1.5.0-SNAPSHOT, you should have the MongoDB Sink Kamelet already installed.

- Run the following commands (for completeness we add the MongoDB Sink Kamelet installation)

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f mongodb-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-mongodb
