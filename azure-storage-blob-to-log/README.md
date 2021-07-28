# Timer to Azure Storage Blob to Log

- Set the credentials options in flow-binding.yaml file for Azure Storage Blob Service

- Run the following commands

kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs azure-storage-blob-to-log
