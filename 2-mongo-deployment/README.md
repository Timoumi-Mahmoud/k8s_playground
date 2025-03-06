## Simple nginx server with k8s using minikube
#### Project overview  

- Mongo and mongo-express deployment using kubernetes minikube.
![Image](Images/arch.png)
```
$ minikube start
```
#### Commands
- creating secret and configmap
- creating deployments, services (internal and external) 

```
$ echo -n "superSecretPwd" | base64 >> secret.yaml
$ echo -n "timoumi" | base64 >> secret.yaml


$ kubectl apply -f mongo-secret.yaml
$ kubectl get secret
$ kubectl describe service mongodb-service
$ kubectl get pod -o wide 
$ kubectl apply -f mongo-express-configmap.yaml
$ kubectl get configmap
```


