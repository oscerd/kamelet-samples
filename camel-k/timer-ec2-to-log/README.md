# Timer EC2 to Log

- The Timer source Kamelet and EC2 Sink are already provided by 1.5.0-SNAPSHOT Camel-K installation

- Set the credentials options in flow-binding.yaml file

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f aws-ec2-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs time-ec2-log
