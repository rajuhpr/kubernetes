## Simple way of creating POD and Services using yaml

### 1. Create a POD using Yaml
```
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  - name: nginx
    image: nginx:1.14.2
    ports:
    - containerPort: 80
```
#### You can refere the below link for more details on POD:
https://kubernetes.io/docs/concepts/workloads/pods/
### 2. Create a service file to expose the pod.
```Servive are used to expose the pods to outside of the world. So, using service ( like, nodeport, clusterIP and LB) We can access the application externally which is running on the POD via browser```
