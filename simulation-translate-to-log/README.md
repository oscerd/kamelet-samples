# Simulation to AWS Translate to Log

- Set correctly the AWS Credentials for AWS translate in the flow-binding file

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f aws-translate-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-translate-to-log
