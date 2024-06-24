# SubQuery Limited Feature Helm Chart

This Helm chart deploys a limited feature version of SubQuery, supporting Node Operators with RPC projects.

## Prerequisites

- Kubernetes 1.19+
- Helm 3.2.0+

## Installing the Chart

1. Clone this repository:

git clone [Your Repository URL]
cd [Repository Directory]

2. Install the chart:

helm install my-release ./my-subql-chart

## Configuration

Modify `values.yaml` for configuration options. Key parameters:

| Parameter | Description | Default |
|-----------|-------------|---------|
| `indexerProxy.replicaCount` | Number of indexer proxy replicas | `2` |
| `coordinator.replicaCount` | Number of coordinator replicas | `1` |
| `ipfs.persistence.size` | IPFS storage size | `10Gi` |

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

helm uninstall my-release

## Support

For issues and feature requests, please file an issue on the GitHub repository.