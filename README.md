# k8s-multi-node-cluster-with-ansible-roles

Build a Kubernetes cluster using Ansible with kubeadm. The goal is to easily install a Kubernetes cluster on machines running RHEL8 and centos on top of AWS public cloud.

# System requirements:

Deployment environment must have Ansible 2.9.0+<br/>
Master and nodes must have passwordless SSH access</br>

# Project-Steps:
 
Step 1 : <br/>
Launching 3 AWS EC2 Instance with Ansible role<br/>
Create Role:<br/>
`ansible-galaxy init ec2`
<br/>
Step 2: <br/>
Setting Up Master Node<br/>
Create Role for setting up the k8s-master node<br/>
`ansible-galaxy init k8s-master`
Step 3 : <br/>
Setting Up Worker Node<br/>
Create Role for setting up the worker-node <br/>
`ansible-galaxy init k8s-worker`

# Verification:

The playbook will download /etc/kubernetes/admin.conf file to $HOME/admin.conf.<br/>

>> Login to the master node.<br/>
>> Verify cluster is fully running using kubectl:<br/>
 
  ```
   kubectl get nodes<br/>
   kubectl get pods<br/>
   kubectl get pods -n "kube-system"<br/>
```
