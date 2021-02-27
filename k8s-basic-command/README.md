## Install Hyperkit and minikube using for MacOS env
* ```brew update```
* ```brew install hyperkit```
* ```brew install minikube```
* ```kubectl``` to verify kubectl already install? 
* ```minikube``` to verify minikube installation successful

## Create minikube cluster
* ```minikube start --vm-driver=hyperkit``` to start minikube with hyperkit
* ```kubectl get nodes``` to get all nodes of minikube
* ```minikube status``` to get status of minikube
* ```kubectl version``` to get version of kubectl install on your machine

## Delete cluster and restart in debug mode
* ```minikube delete``` delete minikube on your machine
* ```minikube start --vm-driver=hyperkit --v=7 --alsologtostderr``` to run minikube with debugs mode
* ```minikube status``` to get status of minikube

## kubectl commands
* ```kubectl get nodes``` to get all nodes existing on your cluster
* ```kubectl get pod``` to get all Pods existing on you cluster with default namespace
* ```kubectl get service``` to get all Service existing on you cluster with default namespace
* ```kubectl create deployment nginx-depl --image=nginx``` to create Deployment with container contains nginx image ```(1)```
* ```kubectl get deployment``` to get all deployment existing on your cluster
* ```kubectl get replicaset``` to get all replicate on you cluster

## Create mongo deployment
* ```kubectl create deployment mongo-depl --image=mongo``` to create Deployment with container contains mongo image
* ```kubectl logs mongo-depl-{pd-name}``` to get logs of Pod
* ```kubectl describe pod mongo-depl-{pod-name}``` to describe Pod

## Delete Deployment
* ```kubectl delete deployment mongo-depl``` to delete Deployment with name is mongo-depl
* ```kubectl delete deployment nginx-depl``` to delete Deployment with name is nginx-depl

## Create or edit config file
* ```vim nginx-deployment.yaml``` to edit Deployment yaml
* ```kubectl apply -f nginx-deployment.yaml``` to apply change for nginx-deployment.yaml

## Delete with config
* ```kubectl delete -f nginx-deployment.yaml``` to delete Deployment create from nginx-deployment.yaml file

# Metrics
* ```kubectl top ``` The kubectl top command return current CPU and Memory usage for a cluster's Pod or nodes, or for a particaluar Pod or node if specific