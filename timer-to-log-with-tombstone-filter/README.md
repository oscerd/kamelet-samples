# Timer to Log with tombstone filter

- Run the following commands

kubectl apply -f timer-no-message-source.kamelet.yaml
kubectl apply -f is-tombstone-filter-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs timer-to-log-with-tombstone
