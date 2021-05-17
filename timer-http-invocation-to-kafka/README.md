# Timer to HTTP to Kafka

- Use the quickstart for https://strimzi.io/quickstarts/ and follow the minikube guide.

- Install camel-k on the kafka namespace

	kamel install -n kafka

- Run the following commands

	kubectl apply -f kafka-not-secured-sink.yaml
	kubectl apply -f flow-binding.yaml

- Check logs

	kamel logs time-http-kafka
