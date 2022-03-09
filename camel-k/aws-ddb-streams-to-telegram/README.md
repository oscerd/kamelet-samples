# AWS DDB Streams to Telegram example

- The DDB Streams Source Kamelet and Telegram sink Kamelet are already provided by camel-k 1.4.0-SNAPSHOT installation

- Set the credentials options in flow-binding.yaml file

- Run the following command

kubectl apply -f flow-binding.yaml

- Check logs

kamel logs ddb-streams-to-telegram
