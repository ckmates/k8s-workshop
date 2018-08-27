# K8S Sock-shop Demo

-  部署 Sock-Shop 網站
-  含有前端, 資料庫, web 透過 AWS Elastic Load Balancer 進入
-  部署專案來源 <https://github.com/microservices-demo/microservices-demo>


## 使用方式

切換到正確目錄 `/k8s-workshop/4.demo/4.4-web-store`

```bash
# create namespace
$ kubectl create namespace sock-shop

# deploy
$ kubectl apply -f sock-shop-demo.yaml

# get pod,services
$ kubectl get pod,services
```

## 刪除方式

```bash
# delete 
$ kubectl delete -f sock-shop-demo.yaml
```

---
# 問題思考

1.  Q: 使用 `kubectl get pod,services` 為什麼看不到相關的資料?
2.  Q: 如何一次找到系統內所有資源? (以pod為例)