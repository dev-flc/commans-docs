# C O M M A N S - K U B E R N E T E S


### Cluster Information

```sh
kubectl version # Show the Kubernetes client and server versions

kubectl cluster-info # Display cluster info

kubectl get nodes # List all nodes in the cluster

kubectl describe node <node-name> # Show detailed information about a specific node
```

### Working with Namespaces

```sh
kubectl get namespaces # List all namespaces

kubectl create namespace <name> # Create a new namespace

kubectl delete namespace <name> # Delete a namespace

kubectl config set-context --current --namespace=<name> # Switch to a specific namespace
```

### Working with Pods

```sh
kubectl get pods # List all pods in the current namespace

kubectl get pods -n <namespace> # List all pods in a specific namespace

kubectl describe pod <pod-name> # Show detailed information about a specific pod

kubectl logs <pod-name> # View logs of a specific pod

kubectl exec -it <pod-name> -- /bin/bash # Access a pod's shell

kubectl delete pod <pod-name> # Delete a specific pod

kubectl get pod <pod-name> -o yaml # Get the YAML configuration of a specific pod
```

### Working with Deployments

```sh
kubectl get deployments # List all deployments in the current namespace

kubectl describe deployment <deployment-name> # Show detailed information about a specific deployment

kubectl create deployment <name> --image=<image> # Create a new deployment

kubectl set image deployment/<deployment-name> <container-name>=<image> # Update the image of a deployment

kubectl scale deployment <deployment-name> --replicas=<number> # Scale a deployment

kubectl rollout status deployment/<deployment-name> # Check the rollout status of a deployment

kubectl rollout undo deployment/<deployment-name> # Rollback to the previous deployment

kubectl delete deployment <deployment-name>  # Delete a specific deployment
```

### Working with Services

```sh
kubectl get services # List all services in the current namespace

kubectl describe service <service-name>  # Show detailed information about a specific service

kubectl expose deployment <deployment-name> --type-NodePort --port=<port> # Expose a deployment as a service

kubectl delete service <service-name> # Delete a specific service
```

### Working with ConfigMaps and Secrets

```sh
kubectl create configmap <name> --from-literal=<key>=<value> # Create a ConfigMap from literal values

kubectl get configmaps # List all Config Maps in the current namespace

kubectl describe configmap <name> # Show detailed information about a specific ConfigMap

kubectl delete configmap <name> # Delete a specific ConfigMap

kubectl create secret generic <name> --from-literal=<key>=<value> # Create a Secret from literal values

kubectl get secrets # List all secrets in the current namespace

kubectl describe secret <name> # Show detailed information about a specific secret

kubectl delete secret <name> # Delete a specific secret
```

### Working with Persistent Volumes (PVs) and Persistent Volume Claims (PVCs)

```sh
kubectl get pv # List all Persistent Volumes in the cluster

kubectl get pvc # List all Persistent Volume Claims in the current namespace

kubectl describe pvc <pvc-name> # Show detailed information about a specific PVC

kubectl delete pvc <pvc-name> # Delete a specific PVC
```

### Working with ReplicaSets
```sh

kubectl get replicasets namespace # List all ReplicaSets in the current namespace

kubectl describe rs <replicaset-name> # Show detailed information about a specific ReplicaSet

kubectl delete rs <replicaset-name> # Delete a specific ReplicaSet
```

### Working with Jobs and CronJobs

```sh
kubectl get jobs # List all jobs in the current namespace

kubectl create job <job-name> --image=<image> # Create a new job

kubectl delete job <job-name> # Delete a specific job

kubectl get cronjobs # List all cron jobs in the current

kubectl create cronjob <name> --schedule="* * * * *" --image=<image> # Create a new cron job with a schedule

kubectl delete cronjob <name> # Delete a specific cron job
```

### Viewing and Debugging Resources

```sh
kubectl get events # List all events in the current namespace

kubectl top nodes # Show resource (CPU/memory) usage of nodes

kubectl top pods # Show resource (CPU/memory) usage of pods

kubectl describe <resource> <name>  # Show detailed information about any resource (e.g., pod, service)
```
### Managing Access Control

```sh
kubectl get roles # List all roles in the current namespace

kubectl get rolebindings  # List all role bindings in the current namespace

kubectl create role <role-name> --verb=get --verb-list --verb=watch --resource=pods # Create a role with specific permissions

kubectl create rolebinding <rolebinding-name> --role=<role-name> --user=<user> # Bind a role to a user

kubectl delete role <role-name> # Delete a specific role

kubectl delete rolebinding <rolebinding-name> # Delete a specific role binding
```

### Miscellaneous

```sh
kubectl apply -f <file.yaml> # Apply changes defined in a YAML configuration file

kubectl delete -f <file.yaml> # Delete resources defined in a YAML configuration file

kubectl edit <resource> <name> # Edit a resource on the fly

kubectl get all # List all resources in the current namespace

kubectl get <resource> -o wide # List resources with additional information (e.g., pods with node info)

kubectl api-resources # List all available resource types in the cluster
```






