# Simulation to LOG with json-schema validator action

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f xj-identity-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-log-with-json-schema-validator
