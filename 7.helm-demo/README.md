## HELM 的基礎指令
使用HELM與Linux套件指令類似, 可簡化在K8S上面部署與升級或是打包遞交的流程  
這邊說明幾個常用指令:

-  helm list (列出已安裝的套件)
-  helm install <Chart> (安裝HELM套件
-  helm delete <Chart> (刪除HELM套件)
-  helm search <Chart> (搜尋HELM套件)

使用這樣的方式, 便可以直接利用網路上做好的Chart來測試部署  


## 建立自己的第一個Chart套件

```bash
# 產生一個demo的Chart套件
$ helm create demo
# 部署剛剛產生的Chart ,名稱demo
$ helm install --name demo demo 
# 取得目前已安裝的Chart
$ helm list 
NAME    REVISION        UPDATED                         STATUS          CHART           APP VERSION     NAMESPACE
demo    1               Tue Aug 21 03:28:41 2018        DEPLOYED        demo-0.1.0      1.0             default

```

## 刪除Chart
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

## 搜尋網路上的Chart
```bash
# 搜尋Chart, 會列出在Chart套件庫內的所有套件
$ helm search 
NAME                                            CHART VERSION   APP VERSION                     DESCRIPTION                                       
coreos/alertmanager                             0.1.7           0.15.1                          Alertmanager instance created by the CoreOS Pro...
coreos/exporter-coredns                         0.0.3                                           A Helm chart for coredns metrics                  
coreos/exporter-kube-api                        0.1.1                                           A Helm chart for Kubernetes                       
coreos/exporter-kube-controller-manager         0.1.10                                          A Helm chart for Kubernetes                       
```

## HELM 參考資源

<https://github.com/helm>  

<https://docs.helm.sh/>  

<https://hub.kubeapps.com/>

