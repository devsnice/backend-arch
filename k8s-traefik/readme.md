helm repo add k8s-at-home https://k8s-at-home.com/charts/
helm install k8s-at-home/traefik-forward-auth
helm install traefik-forward-auth k8s-at-home/traefik-forward-auth --values values.yaml