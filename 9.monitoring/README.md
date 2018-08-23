
## Prometheus

```bash
# 加入 CoreOS Helm repo，為後續安裝做準備
~$ helm repo add coreos https://s3-eu-west-1.amazonaws.com/coreos-charts/stable/

# 建立用於monitoring的namespace 
~$ kubectl create namespace monitoring

# 按照預設組態安裝
~$ helm install coreos/prometheus-operator --name prometheus-operator --namespace monitoring

# 按照預設組態安裝
~$ helm install coreos/kube-prometheus --name kube-prometheus --namespace monitoring  

# 觀察所有的 Pod 是不是已經都 ready 了
~$ kubectl get pod -n=monitoring

# 利用 port forward 從 local 存取 K8S 內的 Grafana Service
~$ kubectl port-forward -n=monitoring svc/kube-prometheus-grafana 8080:80

# 打開瀏覽器連接 
http://localhost:8080 (預設帳密 admin/admin)，底下為 kubernetes-cluster-status Grafana 範本

```