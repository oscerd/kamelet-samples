# Timer to HTTP log

- Run the following commands

kubectl apply -f log-sink.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs time-http-log
