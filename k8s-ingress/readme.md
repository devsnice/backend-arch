1) start munikube
2) kubectl apply -f ./
3) curl http://arch.homework/otusapp/devsnice/health

*Useful commands:*

```
minikube ip
sudo vim  /etc/hosts
kubectl delete service,ingress,deployments,pods --all
kubectl describe pod/pod_name -> check state of Liveness/Readiness
```

kubectl get pods -n kube-system
kubectl logs -n kube-system ingress-nginx-controller-799c9469f7-cnvqv