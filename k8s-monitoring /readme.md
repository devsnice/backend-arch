*How to start*
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm dependency update
helm install backend .

newman run postman-test.json
```

*Monitoring*
```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm install prom prometheus-community/kube-prometheus-stack -f prometheus.yaml --atomic

kubectl port-forward service/prom-grafana 9000:80
kubectl port-forward service/prom-kube-prometheus-stack-prometheus 9090
http://localhost:9090/service-discovery

admin/prom-operator

while true; do ab -n 50 -c 2 http://192.168.64.4:31559/user/7811b36f-d48a-4b51-b781-c6bf5cc4bb52; sleep 3; done

```

*For debug*
```
helm install myapp ./hello-chart --dry-run --debug
helm uninstall backend
helm upgrade backend .
```

*Docs*
https://web.postman.co/collections/13317496-1fab1660-12bf-d13e-1939-e8e6a5c8b4e5?version=latest