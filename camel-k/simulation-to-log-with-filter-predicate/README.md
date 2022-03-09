# Simulation to LOG with predicate filter

- Run the following commands

```
kubectl apply -f predicate-filter-action.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml 
```

- Check logs

```
kamel logs simulation-to-log-with-predicate-filter
```
