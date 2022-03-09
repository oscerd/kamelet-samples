# Simulation to Google Pubsub

- This needs Camel K 1.6.0

- Set the correct credentials for Google Pubsub in the flow-binding.yaml

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f google-pubsub-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-google-pubsub
