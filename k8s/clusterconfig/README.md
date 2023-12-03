
```bash
sudo kubeadm init \
  --control-plane-endpoint wangwenbo.local \
  --upload-certs \
  --pod-network-cidr 172.16.0.0/12 \
  --apiserver-advertise-address 192.168.2.160 \
  --cri-socket unix:///var/run/crio/crio.sock
```



sudo kubeadm init \
  --upload-certs \
  --pod-network-cidr 172.16.0.0/12 \
  --apiserver-advertise-address 192.168.2.160 \
  --cri-socket unix:///var/run/crio/crio.sock



Your Kubernetes control-plane has initialized successfully!

To start using your cluster, you need to run the following as a regular user:

  mkdir -p $HOME/.kube
  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
  sudo chown $(id -u):$(id -g) $HOME/.kube/config

Alternatively, if you are the root user, you can run:

  export KUBECONFIG=/etc/kubernetes/admin.conf

You should now deploy a pod network to the cluster.
Run "kubectl apply -f [podnetwork].yaml" with one of the options listed at:
  https://kubernetes.io/docs/concepts/cluster-administration/addons/

Then you can join any number of worker nodes by running the following on each as root:

kubeadm join 192.168.2.160:6443 --token imsxwz.vr936xjzlvq67k6p \
	--discovery-token-ca-cert-hash sha256:9b0cbafe86837893f559bc2eaee5e182283de1cc7d9f08778221f1fbe181e69f 