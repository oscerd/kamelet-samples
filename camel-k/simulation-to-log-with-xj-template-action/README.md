# Simulation to LOG with xj template action

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f xj-template-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-log-with-xj-template
