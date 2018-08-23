# HELM : The package manager for Kubernetes

-  HELM 是一種K8s的Plugin, 可提供套件安裝與管理
-  類似yum , apt等Linux套件安裝管理工具
-  詳細資訊可以查閱 <https://kairen.github.io/2017/03/25/kubernetes/helm-quickstart/>


## HELM程式安裝
先將最新版的HELM程式拷貝到/usr/local/bin/資料夾

```bash

$ sudo cp helm /usr/local/bin/helm # 拷貝HELM執行檔
$ helm #執行看看

```

## HELM佈署到EKS
部署只需要兩條指令

```bash

$ kubectl apply -f helm.yaml
$ helm init --service-account=helm

```

幾秒後, helm 會佈署 tiller-deploy 的 Pod 於 cluster 內, 可透過指令查看

```bash

$ kubectl get po -n kube-system -l app=helm
NAME                             READY     STATUS    RESTARTS   AGE
tiller-deploy-65bb8478dd-xbqf6   1/1       Running   0          3d

```

