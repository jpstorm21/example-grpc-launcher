# Helm commands

* Crear configuración `helm create <nombre>`
* Aplicar configuración inicial: `helm install <nombre> .`
* Aplicar actualizaciones: `helm upgrade <nombre> .`

# K8s commands

* Obtener pods, deployments y services: `kubectl get <pods | deployments | services>`
* Revisar todos pods: `kubectl describe pods`
* Revisar un pod: `kubectl describe pod <nombre>`
* Eliminar pod: `kubectl delete pod <nombre>`
* Revisar logs: `kubectl logs <nombre>`



# Crear deployment:
```
kubectl create deployment <nombre> --image=<registro/url/imagen> --dry-run=client -o yaml > deployment.yml
```

# Crear service
```
kubectl create service clusterip <nombre> --tcp=<8888> --dry-run=client -o yaml > service.yml 
**kubectl create service nodeport <nombre> --tcp=<3000> --dry-run=client -o yaml > service.yml**
```
* **clusterip**: solo se puede acceder desde dentro del cluster
* **nodeport**: se puede acceder desde fuera del cluster
