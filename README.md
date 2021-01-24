# Aquasecurity helm charts

## Installing helm

```
curl -L https://git.io/get_helm.sh | bash
helm init
```

## Installing aquasecurity charts

```
helm repo add aquasecurity-krol https://krolval.github.io/helm-charts/
helm repo update
helm install my-starboard aquasecurity-krol/starboard
helm status starboard
```