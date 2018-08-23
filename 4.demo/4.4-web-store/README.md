## K8S Sock-shop Demo

| Item | Note |
|:---|:---|
|4.4-web-store | 部署 Sock-Shop 網站, 含有前端, DB, WEB 走 AWS-ELB |

## 使用方式

進入目錄後

```bash
# create namespace
$ kubectl create namespace sock-shop

# deploy sock-shop-demo
$ kubectl apply -f sock-shop-demo.yaml

# get pod,services
$ kubectl get pod,services

# delete 
$ kubectl delete -f sock-shop-demo.yaml
```

## 

Q: 使用 `kubectl get pod,services` 為什麼看不到相關的資料?