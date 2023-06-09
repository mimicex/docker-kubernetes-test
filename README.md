# 透過 docker 在本機端測試 k8s

install kubectl
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/darwin/amd64/kubectl
```
```
chmod +x ./kubectl
```
將kubectl移到PATH下
```
sudo mv ./kubectl /usr/local/bin/kubectl
```
安裝 minikube
```
brew install minikube
```
安裝完之後，可以用 where 指令，查看 minikube 在本機端的安裝位置
```
where minikube
```
啟動 minikube
```
minikube start
```

啟動 minikube 之後，我們可以透過 kubectl run 在 minikube 上運行一個 測試檔案 Google 提供的 hello-minikube 

https://kubernetes.io/docs/tutorials/hello-minikube/
```
kubectl run hello-my-test --image=gcr.io/google_containers/echoserver:1.8 --port=8080
```


# 顯示所有 pods
```
kubectl get pods
```
# 顯示所有 pods labels
```
kubectl get pods --show-labels
```
# 刪除 pod
```
kubectl delete pod hello-my-tes
```