## Nextcloud

This is installed using helm

First create namespace, pvc and ingress

`kubectl apply -f nextcloud.yaml`


`helm repo add nextcloud https://nextcloud.github.io/helm/`


`helm show values nextcloud/nextcloud >> nextcloud.values.yml`


`helm install nextcloud --namespace nextcloud -f nextcloud.values.yml nextcloud/nextcloud`
