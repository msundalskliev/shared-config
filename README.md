# shared-config

Configuration files for deployments.

## Structure

```
deploy/k8s-cluster/dev/
├── shared/
│   └── common-values.yaml    # Single source of truth
├── terraform/
│   └── terraform.yaml        # Terraform-specific config
├── helm/
│   └── helm.yaml            # Helm-specific config
└── configuration.yaml        # Meta configuration
```

## Usage

All tools reference `shared/common-values.yaml` for consistent deployments.