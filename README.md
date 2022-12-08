# Todo list exercise

## Prerequisites 

- [nodejs](https://nodejs.org/en/)
> - [docker](https://docs.docker.com/)
> - [minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/) or any cloud provider to create a cluster

## Install

```sh
git clone https://github.com/thobalose/todo-list-app.git ; cd todo-list-app/
```

```sh
npm install
```

## Run

```sh
node app.js
```

Visit http://localhost:8080 in your browser

## Test

To run tests

```sh
npm test
```

## Docker

To build a docker image for the todo-list-app and run it inside a container execute

```sh
docker build -t dockerhub9876/todo .
```


## Kubernetes

To Apply deployment.yaml

```sh
kubectl apply -f deployment.yaml
```


To Apply service.yaml

```sh
kubectl apply -f service.yaml
```

To Apply deployment.yaml

## Ingress

First and Foremost , Activate Ingress Controller and If you are using Minikube then run :

```sh
minikube addons enable ingress
```


To Apply todo-ingress.yaml

```sh
kubectl apply -f todo-ingress.yaml
```



To validate if your ingress file is applied or not

```sh
kubectl get Ingress
```

To Access the application on browser, navigate to 

```sh
sudo nano /etc/hosts

enter the host name which you have entered on the Ingress yaml file with its ip address.
```
