# Timer to S3 Streaming Upload

- Set the credentials options in flow-binding.yaml file for AWS Service

- Run the following commands

kubectl apply -f aws-s3-streaming-upload-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs timer-to-s3
