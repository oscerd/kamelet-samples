# Bitcoin to Log

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs bitcoin-to-log
