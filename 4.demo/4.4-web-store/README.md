# K8S Sock-shop Demo

部署 Sock-Shop 網站, 含有前端, 資料庫, web 透過 AWS ELB進入

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

## 問題思考

Q: 使用 `kubectl get pod,services` 為什麼看不到相關的資料?