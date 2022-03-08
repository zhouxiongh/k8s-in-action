### 构建容器镜像
```
docker build -t kubia .
```

### 运行容器镜像
```
docker run --name kubia-container -p 8080:8080 -d kubia
```

### 标注镜像
```
docker tag kubia hezx/kubia
```

### 推送镜像
```
docker push hezx/kubia
```
