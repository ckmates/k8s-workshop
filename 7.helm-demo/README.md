## HELM 的基礎指令

-  使用 HELM 與 Linux 套件指令類似, 可簡化在 K8s 部署升級或打包遞交的流程  
-  HELM 使用的部署文件稱為 `Chart`
-  這邊說明幾個常用指令
    -  helm list (列出已安裝的套件)
    -  helm install (安裝HELM套件
    -  helm delete (刪除HELM套件)
    -  helm search (搜尋HELM套件)

使用這樣的方式, 便可以直接利用網路上做好的 Chart 來部署  


## 建立自己的第一個 Chart 套件

```bash
# 產生一個 demo 的 Chart 套件
$ helm create demo

# 部署剛剛產生的 Chart, 名稱 demo
$ helm install --name demo demo 

# 取得目前已安裝的 Chart
$ helm list 
NAME    REVISION        UPDATED                         STATUS          CHART           APP VERSION     NAMESPACE
demo    1               Tue Aug 21 03:28:41 2018        DEPLOYED        demo-0.1.0      1.0             default

```

## 刪除 Chart

```bash
# 取得目前已安裝的Chart
$ helm list 

# 取得目前已安裝的Chart, 含以前所部署過的
$ helm list --all

# 刪除Chart
$ helm delete demo

# 完整刪除Chart
$ helm delete demo --purge 

```

## 搜尋網路上的 Chart

網路上有非常多的 Chart 套件, 可以幫助我們減少重構的時間

```bash
# 搜尋 Chart, 會列出在 Chart 套件庫內的所有套件
$ helm search 
NAME                                            CHART VERSION   APP VERSION                     DESCRIPTION                                       
coreos/alertmanager                             0.1.7           0.15.1                          Alertmanager instance created by the CoreOS Pro...
coreos/exporter-coredns                         0.0.3                                           A Helm chart for coredns metrics                  
coreos/exporter-kube-api                        0.1.1                                           A Helm chart for Kubernetes                       
coreos/exporter-kube-controller-manager         0.1.10                                          A Helm chart for Kubernetes                       
```

## HELM 參考資源

-  <https://github.com/helm>  
-  <https://docs.helm.sh/>  
-  <https://hub.kubeapps.com/>
