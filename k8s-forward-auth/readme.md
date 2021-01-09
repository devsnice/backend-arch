**Schema:**
![Schema of work](auth.drawio.svg?raw=true "Schema of work")

It works if run deployments without hosts (with host: https://github.com/devsnice/backend-arch/pull/1/files)

**Results**
![Test results](results.png?raw=true "Test results")

**Tests:**
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm dependency update
helm install backend .

newman run postman-tests.json
```