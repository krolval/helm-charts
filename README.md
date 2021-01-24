# Aquasecurity Helm Charts

![Aquasecurity logo](https://avatars3.githubusercontent.com/u/12783832?s=200&v=4)

## Introduction

Aquasecurity charts deployment on a [Kubernetes](https://kubernetes.io) cluster using the
[Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.15+ with Beta APIs enabled
- PV provisioner support in the underlying infrastructure

#### Installing helm

```
curl -L https://git.io/get_helm.sh | bash
helm init
```

## Installing charts

### Add repository
```
helm repo add aquasecurity-krol https://krolval.github.io/helm-charts/
helm repo update
```

## Installing the Chart
```
helm install starboard aquasecurity-krol/starboard-operator
helm status starboard
```

### Deploy a specific version

```bash
helm install --name starboard --set image.tag=4.6.2 aquasecurity-krol/starboard-operator
```

### Upgrading chart

```bash
helm upgrade starboard aquasecurity-krol/starboard-operator
```

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `starboard` deployment:

```
$ helm delete starboard
```