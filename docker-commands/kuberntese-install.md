# Install kubernetese in ubuntu
> https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/

> sudo apt-get update
> sudo apt-get install -y apt-transport-https ca-certificates curl 
> sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg

> echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list

> sudo apt-get update
> sudo apt-get install -y kubelet kubeadm kubectl
> sudo apt-mark hold kubelet kubeadm kubectl


# Verify kubectl installation
> kubectl version --client

---------------------------------------
- 5. Join Worker node with master node
--------------------------------------

> kubeadm join 172.31.21.180:6443 --token 5vnrc7.43b5t2licyo75i7i --discovery-token-ca-cert-hash sha256:72748e73d08b45ba92fe8c594b18a8f9183dc46f1ce85b753647746a3beef291