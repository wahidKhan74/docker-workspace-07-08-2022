# Kubernetese Master node setup 
> Kubeadm : Tool to create / initialize cluster

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
  error : 
  > sudo vim /etc/containerd/config.toml
  > commenting out disabled_plugins = ["cri"]

- 3. Assign Unique Hostname
> sudo hostnamectl set-hostname master-node

- 4. Reboot instance.

--------------------------------------
Start Kubernetes Master node( Cluster)
-------------------------------------
> sudo kubeadm init

- output :- Your Kubernetes control-plane has initialized successfully!

- Run as normal user

> mkdir -p $HOME/.kube
> sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
> sudo chown $(id -u):$(id -g) $HOME/.kube/config

or 

- Run as root user

> export KUBECONFIG=/etc/kubernetes/admin.conf

error : connection refuse to localhost:8080 -> echo 'export KUBECONFIG=$HOME/admin.conf' >> $HOME/.bashrc

- 6. Get node.
> kubectl get nodes

