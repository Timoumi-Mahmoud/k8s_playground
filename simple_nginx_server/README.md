## Simple nginx server with k8s using minikube
#### installation guide
```
$ minikube start
$ minikube status

$ kubectl apply -f nginx-deployment.yaml
$ kubectl apply -f nginx-service.yaml
```

- Verifying pods , deployment and service
- curl the homepage of nginx 
```
kubectl get service 
kubectl get deployment
kubectl get pod
kubectl expose deployment nginx-deployment --type=NodePort
minikube ip
curl 192.168.59.100:30258
```



