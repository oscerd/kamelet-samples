# Simulation to LOG with Jsonata Action

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f jsonata-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-log-with-jsonata
