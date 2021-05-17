# Timer to HTTP to Kafka

- Use the quickstart for https://strimzi.io/quickstarts/ and follow the minikube guide.

- Install camel-k on the kafka namespace

	kamel install -n kafka

- Run the following commands

	kubectl apply -f kafka-not-secured-sink.yaml
	kubectl apply -f flow-binding.yaml

- Check logs

	kamel logs time-http-kafka

- Consume from the test-topic

kubectl -n kafka run kafka-consumer -ti --image=quay.io/strimzi/kafka:0.23.0-kafka-2.8.0 --rm=true --restart=Never -- bin/kafka-console-consumer.sh --bootstrap-server my-cluster-kafka-bootstrap:9092 --topic test-topic --from-beginning
If you don't see a command prompt, try pressing enter.
{"number": 7, "message": "success", "people": [{"name": "Mark Vande Hei", "craft": "ISS"}, {"name": "Oleg Novitskiy", "craft": "ISS"}, {"name": "Pyotr Dubrov", "craft": "ISS"}, {"name": "Thomas Pesquet", "craft": "ISS"}, {"name": "Megan McArthur", "craft": "ISS"}, {"name": "Shane Kimbrough", "craft": "ISS"}, {"name": "Akihiko Hoshide", "craft": "ISS"}]}
{"number": 7, "message": "success", "people": [{"name": "Mark Vande Hei", "craft": "ISS"}, {"name": "Oleg Novitskiy", "craft": "ISS"}, {"name": "Pyotr Dubrov", "craft": "ISS"}, {"name": "Thomas Pesquet", "craft": "ISS"}, {"name": "Megan McArthur", "craft": "ISS"}, {"name": "Shane Kimbrough", "craft": "ISS"}, {"name": "Akihiko Hoshide", "craft": "ISS"}]}

