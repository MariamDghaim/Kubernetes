# Kubernetes Summary Task
[![](https://kubernetes.io/images/kubernetes-horizontal-color.png)](https://kubernetes.io/images/kubernetes-horizontal-color.png)


**This repo contains two apps:**
- **BitcoinPrice**
- **YnetNews**

The first app shows the current price of bitcoin and the average price for the last 10 minutes.
The second app displays the latest news from Ynet.

The objective is to deploy the apps in a Kubernetes cluster, it has developed using minikube.

For each website i have used yaml file , which has:
- **Deployment**: build the pod under supervison, so every pod know the docker image to run over.
- **  Service:** enables network access from the cluster or between external clusters. 

------------

## To Run Locally
To deploy both apps on minikube, run the following commands:

1. Clone the project
```
https://github.com/nadeemjazmawe/Kubernetes_Homework.git
```
2. Get in project directory
```
cd Kubernetes
```
 
3. Start minikube
```
minikube start
```
4. Enable ingress on minikube
```
  minikube addons enable ingress
```
5. Finally Insert all deployments
```
 kubectl apply -f .
```
------------

To visit this websites you need to start minikube tunnel 
```
minikube tunnel
```

------------

To visit the websites now using:
```
* http://localhost/bitcoin
* http://localhost/ynet
```

------------

## Stop Minikube ##

To stop minikube:
```
minikube stop
```
To delete your minikube:
```
minikube delete
```


