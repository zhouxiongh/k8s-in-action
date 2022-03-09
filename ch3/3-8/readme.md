### 删除pod

按名称删除

```bash
kubectl delete po kubia-gpu
```

### 使用标签选择器删除pod

```bash
# 删除包含标签creation_method=manual的pod
kubectl delete po -l creation_method=manual
```

### 删除整个命名空间以及pod

```bash
kubectl delete ns custom-namespace
```

### 删除命名空间中的所有pod，但保留命名空间

```bash
kubectl delete po --all
```

### 删除命名空间中的（几乎）所有资源

```bash
kubectl delete all --all
```

