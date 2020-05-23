# Preprequisistes

- Helm 3
- Kubectl client 1.18
- Terraform 1.12.7 


# Steps

1. Install Kubernetes via terraform in GKE

2. Install NGINX via Helm:
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
kubectl create ns management
helm install nginx ingress-nginx/ingress-nginx --namespace management

3. Install Wordpress and Mysql located in /applications/wordpress folder:

```
kubectl apply -k .
```

4. Install Redis in located in /applications/redis folder:
```
kubectl apply -k .
```

