### 创建ReplicationController

```bash
touch kubia-rc.yml
```

```yaml
apiVersion: v1
kind: ReplicationController
metadata: 
   name: kubia
spec: 
   replicas: 3
   selector: 
      app: kubia
   template:
      metadata: 
         labels:
            app: kubia
      spec: 
         containers: 
         - name: kubia
           image: hezx/kubia
           ports: 
           - containerPort: 8080
```

```bash
kubectl create -f kubia-rc.yml
```



### 创建一个服务对象

```bash
kubectl expose rc kubia --type=LoadBalancer --name kubia-http
```



### **列出服务**

```bash
 kubectl get services
```



### **使用外部IP访问服务**

通过服务的外部IP和端口向pod发送请求，**注意** Minikube不支持 LoadBalancer 类型的服务，因此服务不会有外部IP

```bash
minikube service kubia-http
```



## 水平伸缩应用

### **增加期望的副本数**

```bash
kubectl scale rc kubia --replicas=5
```

