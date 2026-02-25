# shared-config

Configuration values for deployments.

## What you get

- Environment-specific config files
- Organized by deployment type
- YAML format for easy editing

## Usage

```bash
terraformlib plan -c shared-config/deploy/k8s-cluster/dev/terraform/terraform.yaml
```

## Structure

```
shared-config/deploy/k8s-cluster/dev/terraform/terraform.yaml
```

## Example config

```yaml
namespace: "monitoring"
cluster:
  name: "monitoring"
  ports:
    grafana: 30080
    influxdb: 30300
helm_chart:
  enabled: true
  name: "monitoring"
  path: "../shared-manifest/deploy/k8s-cluster/dev/helm"
```