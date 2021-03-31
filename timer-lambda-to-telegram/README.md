# Simulation to Dropbox Example

- The Timer source Kamelet, Lambda Sink Kamelet and Telegram sink is already provided is already provided by camel-k 1.4.0-SNAPSHOT installation

- Set the credentials options in flow-binding.yaml file

- Run the following commands

kubectl apply -f flow-binding.yaml

- Check logs

kamel logs time-lambda-telegram
