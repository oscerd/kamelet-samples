# Minikube setup

- Clone camel-k repository
- Spin up a minikube cluster
- minikube start
- Set up registry
- minikube addons enable registry
- Use the minikube docker env
- eval $(minikube docker-env)
- Build camel k
- make images
- install camel-k on minikube
- ./kamel install --maven-repository https://repository.apache.org/content/repositories/snapshots@id=apache-snapshots@snapshots 
- Check if everything is working fine
- kubectl get ip
- Install kamelets and flows
