# Simulation to LOG with hoist field action

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f hoist-field-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-log-with-hoist-field
