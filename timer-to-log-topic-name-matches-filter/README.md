# Timer to Log with topic name matches action

- Run the following commands

kubectl apply -f topic-name-matches-filter-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs timer-to-log
