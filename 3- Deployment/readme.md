##  Deployment is an Object and its super set of all other object in K8's
```Deployment: we defined the desired resources in one file. Usually we will create a replicaset - min, max, desired - on deployment file instead of creating seperate replicasSet file. Some cases we can edit the deloyments in cluster level using below command```

``` kubectl edit deployment <deployment-name> -n namespace ```

### ```Service file``` ####
```Service is used to expose the deployments to the outside of the world by specifing the service type and ports like```
##### ```port: 80 service port,  targetPort: 80 containerPort, nodePort: 31233``` #####
