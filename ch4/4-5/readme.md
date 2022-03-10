### 运行多个job

顺序运行5个任务

```yaml
spec:
   completions: 5
```

并行运行

```yaml
spec:
   completions: 5
   parallelism: 2
```

Job 的缩放

```bash
$ kubectl scale job multi-completion-batch-job --replicas 3
```

