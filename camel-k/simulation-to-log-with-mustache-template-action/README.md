# Simulation to LOG with mustache template action

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f mustache-template-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs mustache-sample
