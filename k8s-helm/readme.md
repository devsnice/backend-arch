*How to start*
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm dependency update
helm install backend .
```

*For debug*
```
helm install myapp ./hello-chart --dry-run --debug
helm uninstall backend
helm upgrade backend
```