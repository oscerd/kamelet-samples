# Simulation to Azure Storage Blob

- The Azure Storage Blob Source Kamelet is already provided by camel-k 1.4.1-SNAPSHOT installation

- Set the credentials options in flow-binding.yaml file

- Run the following commands

kubectl apply -f azure-storage-blob-sink.kamelet.yaml
kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-azure-storage-blob
