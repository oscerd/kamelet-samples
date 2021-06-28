# MongoDB to Log

- Set the correct credentials for MongoDB instance in the flow-binding.yaml

- Run the following commands

kubectl apply -f mongodb-source.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml 

- Check logs

kamel logs s3-to-kafka-with-timestamp-router -n kafka
