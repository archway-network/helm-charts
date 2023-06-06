# Endpoint Controller

Kubernetes Endpoint Controller is a program written in Golang that watches Kubernetes service annotations and creates Kubernetes endpoints based on those annotations. This program is meant to watch Cosmos blockchain nodes and determine their health and dynamically remove/add endpoint targets.

Controller will generate Endpoint with correct targets and port assignments based on annotations and service resource.

## Prerequisites

Kubernetes 1.16+

## Get Repository Info

```console
helm repo add prometheus-community https://archway-network.github.io/helm-charts
helm repo update
```

_See [`helm repo`](https://helm.sh/docs/helm/helm_repo/) for command documentation._

## Install Chart

```console
helm install [RELEASE_NAME] archway-network/endpoint-controller
```

_See [configuration](#configuration) below._

_See [helm install](https://helm.sh/docs/helm/helm_install/) for command documentation._

## Uninstall Chart

```console
helm uninstall [RELEASE_NAME]
```

This removes all the Kubernetes components associated with the chart and deletes the release.

_See [helm uninstall](https://helm.sh/docs/helm/helm_uninstall/) for command documentation._

## Upgrading Chart

```console
helm upgrade [RELEASE_NAME] [CHART] --install
```

_See [helm upgrade](https://helm.sh/docs/helm/helm_upgrade/) for command documentation._

## Configuration

See [Customizing the Chart Before Installing](https://helm.sh/docs/intro/using_helm/#customizing-the-chart-before-installing). To see all configurable options with detailed comments, visit the chart's [values.yaml](./values.yaml), or run these configuration commands:

```console
helm show values archway-network/endpoint-controller
```
