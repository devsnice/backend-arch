Problems:

```
192.168.64.1 - - [05/Jan/2021:19:22:13 +0000] "POST /auth/login HTTP/1.1" 200 9 "-" "PostmanRuntime/7.26.5" 379 0.294 [default-backend-auth-service-80] [] 172.17.0.10:8080, 172.17.0.11:8080 0, 9 0.001, 0.293 502, 200 006cc2f6e7e6c96f4be2ec611848d00b
192.168.64.1 - - [05/Jan/2021:19:22:13 +0000] "GET /api/user/4bbf1ff6-8925-4768-80bd-141b83f3bb51 HTTP/1.1" 502 0 "-" "PostmanRuntime/7.26.5" 0 0.000 [default-backend-app-service-80] [] 10.103.201.12:80 0 0.000 502 233b8d5b6161c12265699ff3bd421c5f
192.168.64.1 - - [05/Jan/2021:19:22:13 +0000] "GET /api/user/4bbf1ff6-8925-4768-80bd-141b83f3bb51 HTTP/1.1" 500 177 "-" "PostmanRuntime/7.26.5" 298 0.000 [default-backend-app-service-80] [] - - - - 233b8d5b6161c12265699ff3bd421c5f
2021/01/05 19:22:13 [error] 24204#24204: *1115589 connect() failed (111: Connection refused) while connecting to upstream, client: 192.168.64.1, server: arch.homework, request: "GET /api/user/4bbf1ff6-8925-4768-80bd-141b83f3bb51 HTTP/1.1", subrequest: "/_external-auth-L2FwaS8oLiop", upstream: "http://10.103.201.12:80/auth", host: "arch.homework"
2021/01/05 19:22:13 [error] 24204#24204: *1115589 auth request unexpected status: 502 while sending to client, client: 192.168.64.1, server: arch.homework, request: "GET /api/user/4bbf1ff6-8925-4768-80bd-141b83f3bb51 HTTP/1.1", host: "arch.homework"
```
It works if run deployments without hosts


Tests:
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm dependency update
helm install backend .

newman run postman-tests.json
```