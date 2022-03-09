# Google Pubsub to Log

- This needs Camel K 1.6.0

- Set the correct credentials for Google Pubsub in the flow-binding.yaml

- Run the following commands

kubectl apply -f google-pubsub-source.kamelet.yaml
kubectl apply -f flow-binding.yaml 

- Check logs

kamel logs google-pubsub-to-log
