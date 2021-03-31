# Simulation to Dropbox Example

- The Dropbox Sink Kamelet is already provided by camel-k 1.4.0-SNAPSHOT installation

- Set the credentials options in flow-binding.yaml file

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f set-header.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-aws-sqs
