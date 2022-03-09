# Simulation to LOG with extract field action

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f extract-field-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-log-with-extract-field
