# Timer to Log with filter

- Run the following commands

kubectl apply -f has-header-filter-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs timer-to-log
