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

The replicaCount is not a standard configuration option for the Nginx Ingress Helm chart, and Nginx Ingress Controller pods are typically scaled horizontally based on demand rather than a fixed count.
<br />
to make more pods, do this:

 - ```kubectl edit deployment <nginx-ingress-deployment-name> -n default```
 - ```edit the replica to desired number, in my case 10. replica: 10```
 - ```save it and you are done```
