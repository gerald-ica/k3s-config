# K3s Cluster Configuration

This repository contains Kubernetes manifests for the K3s cluster, managed by [Config Sync](https://cloud.google.com/anthos-config-management/docs/config-sync-overview).

## Structure

```
.
├── cluster/           # Cluster-wide resources
├── namespaces/        # Namespace-scoped resources
│   ├── production/
│   └── staging/
└── README.md
```

## How it works

Config Sync automatically syncs this repository to the K3s cluster. Any changes pushed to the `main` branch will be applied within seconds.

## Adding resources

1. Create a YAML manifest in the appropriate directory
2. Commit and push to `main`
3. Config Sync will automatically apply the changes

## Cluster Details

- **Cluster**: proxmox-k3s
- **Nodes**: 9 (hybrid on-prem + GCP)
- **Fleet**: informal-dcp
