*How to start*
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm dependency update
helm install backend .

newman run postman-test.json
```

*For debug*
```
helm install myapp ./hello-chart --dry-run --debug
helm uninstall backend
helm upgrade backend
```

*Docs*
https://web.postman.co/collections/13317496-1fab1660-12bf-d13e-1939-e8e6a5c8b4e5?version=latest