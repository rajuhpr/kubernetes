**We can create a EKS cluster using declarative and imperative approach.** 

eksctl create cluster eksdemo --region=us-east-1 --zones=us-east-1a,us-east-1b  --without-nodegroup

**#Get created nodes**

kubectl get nodes

**#Get List of clusters**

eksctl get cluster

**#Associate IAM OIDC Provider for EKS cluster:**

eksctl utils associate-iam-oidc-provider --region us-east-1 --cluster eksdemo1 --approve
#Create a Node Group with additional add-on’s on Public Subnets:
eksctl create nodegroup --cluster=eksdemo --region=us-east-1 --name=eksdemo1-ng-public1 --node-type=t3.medium --nodes=2 --nodes-min=2 --nodes-max=4 --node-volume-size=20 --ssh-access --ssh-public-key=kube-demo --managed --asg-access --external-dns-access --full-ecr-access --appmesh-access --alb-ingress-access

**#List EKS clusters**

eksctl get cluster

**#List NodeGroups in a cluster**

eksctl get nodegroup --cluster=<clusterName>

**#List of Nodes in current kubernetes cluster**

kubectl get nodes -o wide

**#Our kubectl context should be automatically changed to new cluster**

kubectl config view –minify
