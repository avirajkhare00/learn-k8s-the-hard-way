## Installation of nginx controller using helm

Helm is a package manager for Kubernetes.

To cover:
 - creation of nginx proxy using helm
 - install helm on your machine, Google it :)
 - install nginx chart

Not to cover:
 - mapping custom domain to load balancer


## Commands
 - ```helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx```
 - ```helm repo update```
 - ```helm install nginx-ingress ingress-nginx/ingress-nginx -f values.yaml```
 -

## To read
 - https://helm.sh/
 - https://github.com/kubernetes/ingress-nginx

## To Debug
 - why 1 pod?
