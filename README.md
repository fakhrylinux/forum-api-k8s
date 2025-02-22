# K8s project to Deploy forum API

## How to run this project
Install [minikube](https://minikube.sigs.k8s.io/docs/) and [kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl). And follow these instruction.
- Start minikube
```sh
minikube start
```
- Create namespace
```sh
kubectl apply -f ns
```
- Apply declarative file for forum-api and postgres
```sh
kubectl apply -f forum-api -f postgres
```
- Get all results and note the port number for `forum-api-server` service
```sh
kubectl get all -n forum-api
```
Example:

![kubectl comand](https://i.imgur.com/3D5mnLZ.png)
- Get the cluster ip address
```sh
minikube ip
```

Then you can access the API at `http://<minikube-ip>:<forum-api-server-port>`

Related project:
[Forum API](https://github.com/fakhrylinux/forum-api)

