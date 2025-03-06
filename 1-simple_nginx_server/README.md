## Simple nginx server with k8s using minikube
- Kubernetes deployment and service for an nginx server.
#### Requirements 
- minkikube
- kubectl 
- VirtualBox
```
$ minikube version
$ kubectl version 
```
#### Commands

- Creating deployment and service 
- expose internal service to become NodePort 
- Verifying pods , deployment and service
- curl the homepage of nginx 


```
$ kubectl apply -f nginx-deployment.yaml
$ kubectl apply -f nginx-service.yaml

kubectl get service 
kubectl get deployment
kubectl get pod

kubectl expose deployment nginx-deployment --type=NodePort

minikube ip
curl 192.168.59.100:30258
```



#### Clean-up

kubectl delete -f nginx-service.yaml
kubectl delete -f nginx-deployment.yaml
