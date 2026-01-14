# helm-trivy-operator

Installs the [Aqua Security Trivy Operator](https://github.com/aquasecurity/trivy-operator) Helm chart using Crossplane and the Helm provider.

## Features

Trivy Operator provides comprehensive security scanning for Kubernetes:

- **Vulnerability Scanning** - Scan container images for known vulnerabilities
- **SBOM Generation** - Generate Software Bill of Materials for containers
- **Misconfiguration Detection** - Detect Kubernetes misconfigurations
- **Exposed Secrets Scanning** - Find secrets exposed in container images
- **RBAC Assessment** - Assess RBAC configurations for security issues
- **Infrastructure Assessment** - Evaluate infrastructure security

## Usage

```yaml
apiVersion: helm.hops.ops.com.ai/v1alpha1
kind: TrivyOperator
metadata:
  name: trivy-operator
  namespace: my-namespace
spec:
  clusterName: my-cluster
```

## Configuration

| Field | Description | Default |
|-------|-------------|---------|
| `spec.clusterName` | Name of the target cluster | Required |
| `spec.namespace` | Namespace for the Helm release | `trivy-system` |
| `spec.name` | Helm release name | XR metadata.name |
| `spec.labels` | Custom labels merged with defaults | `{}` |
| `spec.values` | Helm values merged with defaults | `{}` |
| `spec.overrideAllValues` | Helm values replacing all defaults | `{}` |
| `spec.providerConfigRef.name` | ProviderConfig name | `clusterName` |
| `spec.providerConfigRef.kind` | ProviderConfig kind | `ProviderConfig` |

## Examples

See the `examples/` directory for usage examples:

- `minimal.yaml` - Basic installation
- `standard.yaml` - Installation with all scanners enabled and resource limits
