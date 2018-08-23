## kubectl 常用指令參考

完成kubectl設定後, 會透過`bash completion`來幫助我們使用kubectl 指令
無需去記所有的指令, 只需要在適當的時機使用 `--help` 來查閱指令的用法即可
這邊列出幾個常用的指令, 更多指令與用途可到官網查詢
<https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands>

使用指令縮寫可減少打字, 建議初學仍需要瞭解整個指令較好, 查閱縮寫 `$ kubectl api-resources`

-  kubectl get（取得資源）
-  kubectl create namespace（建立 namespace）
-  kubectl run（建立容器映像）
-  kubectl label（更新資源的label）
-  kubectl replace（替換資源）
-  kubectl scale（手動擴充容器數量）
-  kubectl edit (編輯資原)
-  kubectl expose（將資源暴露為新的 Service，可供對外存取）
-  kubectl delete（删除資源）
-  kubectl create service（建立 Service）
-  kubectl rolling-update（進行滾動更新）
-  kubectl rollout pause（暫停更新）
-  kubectl rollout resume（恢復更新）
-  kubectl rollout status（查詢更新的資源狀態）
-  kubectl rollout undo（回滾之前版本）
-  kubectl rollout history（取得歷史版本）
