Problems:

1) nginx cannot resolve doma

https://github.com/kubernetes/ingress-nginx/issues/1416


TODO:
1) understand how to define forward-auth host for nginx
2) draw scheme of work

Tests:
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm dependency update
helm install backend .

newman run postman-tests.json
```