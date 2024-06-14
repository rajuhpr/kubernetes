## Kuberenetes Cluster
  
  - Cluster is a Group of computing nodes or worker machines that run containerized applications.
  - Kubernetes is an open source system for automating deployment, scaling, and management of containerized applications
   

  
 
![image](https://github.com/rajuhpr/kubernetes/assets/142870952/b8520455-79ff-4692-adf9-36f4762950ff)


## Control Plane:
The control plane's components make global decisions about the cluster (for example, scheduling), as well as detecting and responding to cluster events (for example, starting up a new pod when a Deployment's replicas field is unsatisfied).
Control plane components can be run on any machine in the cluster and do not run user containers on this machine. 

1.	### Kube-Api-server:
     It’s a component of the Kubernetes control plane that exposes the Kubernetes API.
   	 In other words, The Kube-API server is the front end for the Kubernetes control plane.
2.	### etcd:
	   It’s a consistent and highly available Key-value storage for storing all cluster information data. (Master and worker node)
4.	### Kube scheduler:
     Its responsible for distribute the containers across the node.It watches newly created PODs with no assigned node, and select a node for them to run.
5.	### Kube controller Manager:
     Controllers are responsible for notice and responding when nodes, containers or endpoints go down. They make decision to spirn-up new container. 
      
        ### Kube-controllers are the combination of multiple controllers
  	
      ```
      • Node controller: Responsible for notice and responding when nodes go down.
      •	Replication controller: Responsible for maintaining the correct no. of pods for every replication controller.
      •	Endpoint controller:  Populate the end point Objects.
      •	Service account, Token controller: Create default account and API access for new Namespaces.
      ```
7.	### Cloud-controller –manager:
       A kubernetes control plane components embeds cloud-specific control logic.
       ```
      •	It only run on controller those are specific to cloud providers.
      •	On-premise K8’s clusters will not have this component.
      •	Node-controller: For checking the cloud provider to determine if node has been deleted in cloud after it is stop responding.
      •	Route controller: Setting up routes in the underlying cloud infrastructure.
      •	Service controller: Creating, updating and deleting cloud provider Load Balancer.
       ```
## Worker Node Architecture:

  ### Worker node mainly contain Kubelet and kube-proxy.
  
  #### 1. Kubelet: 
    Kubelet is an Agent, runs on every node on cluster.	
    This make sure, Containers are running are running in a POD on a node.

  #### 2. Kube-proxy:
    It’s a n/w proxy that runs on each node in your cluster. 
    It maintains network rule, Allow n/w communication to your pods from n/w session inside/outside of your cluster.


       
