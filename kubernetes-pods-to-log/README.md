# Kubernetes Namespace Watcher to Log

- Set the correct token for your Kubernetes Cluster

- Ensure the Kubernetes user you're using has the correct permission to watch, list and get namespaces resource.

- If you are on Minikube, for your convenience you can use the cluster role binding defined in cluster-role-binding-default.yaml

kubectl apply -f cluster-role-binding-default.yaml
kubectl create clusterrolebinding service-reader-pod --clusterrole=service-reader --serviceaccount=default:default

- Run the following commands

kubectl apply -f kubernetes-namespace-source.kamelet.yaml
kubectl apply -f log-sink.kamelet.yaml
kubectl apply -f flow-binding.yaml 

- Check logs

kamel logs namespace-to-log
