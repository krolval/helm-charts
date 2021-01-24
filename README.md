# helm-charts
Aquasecurity helm charts

## Install a helm chart (v3) from aquasecurity repository

```
curl -L https://git.io/get_helm.sh | bash
helm init
helm repo add aquasecurity-krol https://krolval.github.io/helm-charts/
helm repo update
helm install my-starboard aquasecurity/starboard
helm status starboard
```