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
| `coordinator.disableManagedProjects` | Disable the feature to create managed SubQL projects | `true` |
| `coordinator.showStdoutInAdminUI` | Show coordinator's stdout in admin UI | `false` |
| `ipfs.persistence.size` | IPFS storage size | `10Gi` |

### Important Notes

- When `coordinator.disableManagedProjects` is set to `true`, the ability to create new managed SubQL projects through the admin UI will be disabled. This is recommended for Kubernetes deployments where creating containers through docker sock is not possible.
- `coordinator.showStdoutInAdminUI` controls whether the coordinator's stdout is displayed in the admin UI. Set to `false` to hide it, which may be necessary in Kubernetes environments.

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

helm uninstall my-release

## Support

For issues and feature requests, please file an issue on the GitHub repository.