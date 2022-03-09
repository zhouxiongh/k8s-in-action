### 给ReplicationController管理的pod加标签

```bash
kubectl label po kubia-b429t type=sp
```

### **更改已托管的pod的标签**

```bash
$ k label po kubia-nkw5r app=foo --overwrite
```

### 修改pod模板

```bash
$ k edit rc kubia
```

### 删除一个ReplicationController 不删除pod

```bash
$ k delete rc kubia --cascade=false
```

