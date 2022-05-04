# Port-forward minio service
```
kubens minio
kg svc
kubectl port-forward svc/minio 9001
```

# Getting minio ui login credentials(username + password)
```
kubectl -n minio get secret minio -o jsonpath="{.data.root-user}" | base64 -d; echo
kubectl -n minio get secret minio -o jsonpath="{.data.root-password}" | base64 -d; echo
```
