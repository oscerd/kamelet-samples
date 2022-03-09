# S3 to Log with secrets

- Run the following command to create the secret related to AWS S3 credentials

  kubectl create secret generic aws-s3-secret --from-literal=accessKey=<accessKey> --from-literal=secretKey=<secretKey>

- Run the following commands

  kubectl apply -f log-sink.kamelet.yaml
  kubectl apply -f flow-binding.yaml 

- Check logs

  kamel logs s3-to-log-with-secret
