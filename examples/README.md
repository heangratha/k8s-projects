# Common Kubernetes object

## Kubernetes commands

    kubectl apply, delete, get, describe, log, exec, cp
    kubectl exec -it <pod-name> -- /bin/bash

## 1. configmap

    kubectl apply -f 1-configmap.yml
    kubectl delete -f 1-configmap.yml
    kubectl get configmap, cm

## 2. Persistance Volume

    kubectl apply -f 2-persistanceVolume.yml

## 3. Persistance Volume Claim

    kubectl apply -f 3-persistanceVolumeClaim.yml

## 4. Deployment and pod

    kubectl apply -f 4-nginx-deployment.yml

## 5. Services

    kubectl apply -f 5-nginx-service.yml

## 6. Nginx Ingress

    kubectl apply -f 6-nginx-ingress.yml

## port-forwarding

    kubectl get po
    kubectl port-forward <pod-name> 80:80