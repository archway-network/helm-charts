# Lambo Proxy

## Prerequisites

Kubernetes 1.16+

## Get Repository Info

```console
helm repo add archway-network https://archway-network.github.io/helm-charts
helm repo update
```

_See [`helm repo`](https://helm.sh/docs/helm/helm_repo/) for command documentation._

## Install Chart

```console
helm install [RELEASE_NAME] archway-network/lambo-proxy
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
helm show values archway-network/lambo-proxy
```

### Configuration Parameters

The chart supports the following main configuration sections:

- `image`: Container image configuration (repository, tag, pullPolicy)
- `replicaCount`: Number of replicas to deploy
- `resources`: CPU and memory limits/requests
- `config`: Application configuration (proxy_port, health_check_interval, backend_addresses, etc.)
- `service`: Service configuration (port, type)
- `serviceMonitor`: Prometheus ServiceMonitor configuration (enabled, interval, etc.)
- `ingress`: Ingress configuration (enabled, hosts, annotations, tls)

