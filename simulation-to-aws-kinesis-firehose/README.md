# Simulation to AWS Kinesis Firehose Sink Example

- The AWS Kinesis Firehose Sink Kamelet is already provided by camel-k 1.4.0-SNAPSHOT installation

- Set the credentials options in flow-binding.yaml file

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f aws-kinesis-firehose-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-aws-kinesis-firehose
