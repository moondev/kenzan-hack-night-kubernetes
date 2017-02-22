## Clone this repo

`git clone https://github.com/moondev/kenzan-hack-night-kubernetes.git hacknight; cd hacknight`

## Start local kubernetes cluster

`minikube start --memory 4000`

## Wait for all pods to start

`kubectl get pods --all-namespaces`

## Launch the dashboard

`minikube dashboard`

## Install the registry

`kubectl apply -f registry.yml`

## Install Jenkins

`kubectl apply -f jenkins.yml`

## Setup Jenkins

`kubectl port-forward jenkins 8888:8080`

* turn off cross-site forgery protection

### get jenkins admin token

`kubectl exec jenkins cat /root/.jenkins/secrets/initialAdminPassword | pbcopy`

## Install Gogs

`kubectl apply -f gogs.yml`

## Setup Gogs

`kubectl port-forward gogs 3000:3000`

`open http://localhost:3000`

### Create repo