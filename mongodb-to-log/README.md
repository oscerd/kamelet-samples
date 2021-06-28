# S3 to Log

- Set the correct credentials for S3 in the flow-binding.yaml

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml 

- Check logs

kamel logs s3-to-kafka-with-timestamp-router -n kafka
