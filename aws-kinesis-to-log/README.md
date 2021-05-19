# AWS Kinesis to Log example

- Set the credentials options in flow-binding.yaml file for AWS Kinesis

- Run the following command

kubectl apply -f log-sink.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs aws-kinesis-to-log
