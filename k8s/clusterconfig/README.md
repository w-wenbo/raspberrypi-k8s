
```bash
sudo kubeadm init \
  --control-plane-endpoint wangwenbo.local \
  --upload-certs \
  --pod-network-cidr 172.16.0.0/12 \
  --apiserver-advertise-address 192.168.2.160 \
  --cri-socket unix:///var/run/crio/crio.sock
```