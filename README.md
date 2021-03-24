# k8s-multi-node-cluster-with-ansible-roles

Build a Kubernetes cluster using Ansible with kubeadm. The goal is to easily install a Kubernetes cluster on machines running RHEL8 and centos on top of AWS public cloud.

# System requirements:

Deployment environment must have Ansible 2.9.0+<br/>
Master and nodes must have passwordless SSH access</br>

# Verification:

The playbook will download /etc/kubernetes/admin.conf file to $HOME/admin.conf.<br/>

>> Login to the master node.<br/>
>> Verify cluster is fully running using kubectl:(<-- two spaces)
 
   [snippet]
   1.kubectl get nodes<br/>
   2.kubectl get pods<br/>
   3.kubectl get pods -n "kube-system"<br/>
