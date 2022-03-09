# Bitcoin to S3

- In the flow binding file insert the AWS Credentials and the bucket name

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs bitcoin-to-s3
