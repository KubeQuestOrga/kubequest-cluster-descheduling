# KubeQuest - Descheduling Cluster K3S

## ⚙️ Setup Environment
1. Connect to the NODE MASTER in Cluster K3S.
2. Install HELM : https://helm.sh/docs/intro/install/
3. Use repo Descheduling Helm : https://artifacthub.io/packages/helm/descheduler/descheduler?modal=install
4. Run command add repo Descheduling and install :
```bash
sudo chmod 644 /etc/rancher/k3s/k3s.yaml
sudo helm repo add descheduler https://kubernetes-sigs.github.io/descheduler/
sudo helm repo update
sudo KUBECONFIG=/etc/rancher/k3s/k3s.yaml helm install descheduler descheduler/descheduler --namespace descheduler --create-namespace --version 0.30.1 --values values.yaml
```

<br /><br /><br /><br />


## 🚀 Update chart Descheduling HELM for values.yaml
1. Connect to the NODE MASTER in Cluster K3S.
2. Run command :
```bash
sudo chmod 644 /etc/rancher/k3s/k3s.yaml
sudo KUBECONFIG=/etc/rancher/k3s/k3s.yaml helm upgrade descheduler descheduler/descheduler --namespace descheduler --values values.yaml
```
