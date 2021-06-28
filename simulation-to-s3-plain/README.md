# Simulation source to S3 Plain

- Add the correct credentials to the flow-binding file

- Using camel-k 1.5.0-SNAPSHOT all the needed Kamelets are already included within the installation

- Run the following commands

kubectl apply -f simulation-source.kamelet.yaml
kubectl apply -f flow-binding.yaml

- Check logs

kamel logs simulation-to-s3-plain
