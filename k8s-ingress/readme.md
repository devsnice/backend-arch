1) start munikube
2) kubectl apply -f ./
3) curl http://arch.homework/otusapp/devsnice/health

*Useful commands:*

```
minikube ip
sudo vim  /etc/host
kubectl delete service,ingress,deployments,pods --all
kubectl describe pod/pod_name -> check state of Liveness/Readiness
```