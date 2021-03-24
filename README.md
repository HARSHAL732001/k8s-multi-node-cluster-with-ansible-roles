# k8s-multi-node-cluster-with-ansible-roles

Build a Kubernetes cluster using Ansible with kubeadm. The goal is to easily install a Kubernetes cluster on machines running RHEL8 and centos on top of AWS public cloud.

# System requirements:

1.Deployment environment must have Ansible 2.9.0+ 
2.Master and nodes must have passwordless SSH access

# Verification:

The playbook will download /etc/kubernetes/admin.conf file to $HOME/admin.conf.

>> Login to the master node.
>> Verify cluster is fully running using kubectl:
 
   1.kubectl get nodes
   2.kubectl get pods
   3.kubectl get pods -n "kube-system"
