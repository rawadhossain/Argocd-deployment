# Argocd Deployment
## Gitops and Agrocd deployment 

![alt text](image\image.png)

## Install Argocd locally
```
kubectl create namespace argocd
```
```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```
Pods and Services initiated by Agrocd
![alt text](image\image-1.png)

## Access the Argocd UI and Port Forwarding
Port Forwarding   which lets you port forward on your local machine to an internal service running in K8s
![alt text](image\image-2.png)
```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```
## Debugging
```
kubectl logs -n argocd deployment/argocd-application-controller
```
## Agrocd automatically started pods based on the commits on manifest.yml
![alt text](image\image-3.png)
