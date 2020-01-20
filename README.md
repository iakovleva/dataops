## Prerequisites

- git clone https://github.com/iakovleva/dataops

- Install [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

- Install [Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/)

- Build Docker image. Run the command from the same directory where is docker-compose.yml

```docker-compose build```

## 1. Create a Minikube cluster

Start up a local Kubernetes cluster with minikube

```minikube start --vm-driver=<driver_name>```

Access the Kubernetes Dashboard

```minikube dashboard```


## 2. Create a Deployment

```kubectl apply -f deployment.yml```


## 3. Create a service so that you can access the application from outisde the cluster.

```kubectl expose deployment/helloworld --type=NodePort --port 5000```


## 4. Start the app:

```minikube service helloworld```
