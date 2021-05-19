# HTTP Source to log

- Run the following commands

kubectl apply -f http-secured-source.yaml
kubectl apply -f log-sink.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs secure-http-log
