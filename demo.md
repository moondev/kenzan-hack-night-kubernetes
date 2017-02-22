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

## Install Gogs

`kubectl apply -f gogs.yml`

## Setup Gogs