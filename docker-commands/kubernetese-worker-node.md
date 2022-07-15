# Kubernetese Node node setup 
> Kubectl : Tool to connect to kubernetese cluster

- 1. Disable the swap memmory
> sudo swapoff -a 
> sudo sed -i '/ swap / s/^/#/' /etc/fstab

- 2. Add Kubernetes cgroup
> sudo vim /etc/docker/daemon.json 
> { "exec-opts": ["native.cgroupdriver=systemd"] } 
> sudo systemctl daemon-reload 
> sudo systemctl restart docker 
> sudo systemctl restart kubelet 
> sudo docker info |grep -i cgroup

- 3. Assign Unique Hostname
> sudo hostnamectl set-hostname worker01 or 
> sudo hostnamectl set-hostname worker02

- 4. Reboot instance.

---------------------------------------
- 5. Join Worker node with master node
--------------------------------------

> kubeadm join 172.31.21.180:6443 --token 5vnrc7.43b5t2licyo75i7i --discovery-token-ca-cert-hash sha256:72748e73d08b45ba92fe8c594b18a8f9183dc46f1ce85b753647746a3beef291