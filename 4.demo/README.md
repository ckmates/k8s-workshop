## K8S-DEMO

| Item | Note |
|:---|:---|
|4.1-nginx | 部署 NGINX 服務 |
|4.2-node-selector | 透過 label 來選擇 node |
|4.3-rolling-update | 透過 rolling-update 更新 |
|sock-shop-demo.yaml | 部署Sock-Shop網站, 含有前端, DB 走 ELB進入 |

## 使用方式

進入目錄後

```bash
# deploy sock-shop-demo
$ kubectl apply -f sock-shop-demo.yaml

# get pod,services
$ kubectl get pod,services

# delete 
$ kubectl delete -f sock-shop-demo.yaml
```

