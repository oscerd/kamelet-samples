# Simulation to AWS SNS FIFO Example

- The AWS SNS FIFO Sink Kamelet is already provided by camel-k 1.4.0-SNAPSHOT installation

- Set the credentials options in flow-binding.yaml file

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-aws-sns
