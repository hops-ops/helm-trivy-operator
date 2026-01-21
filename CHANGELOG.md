### What's changed in v0.1.0

* feat: initial trivy-operator helm xrd configuration (by @patrickleet)

* feat: helm chart xrd (by @patrickleet)

* feat(deps): update crossplane-contrib/provider-helm docker tag to v1.0.6 (#1) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* chore(deps): update unbounded-tech/workflow-vnext-tag action to v1.21.0 (#3) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* fix(e2e): add RBAC and improve e2e test configuration (by @patrickleet)

  - Add ClusterRoleBinding for crossplane-system cluster-admin
  - Generate unique test names using timestamp to avoid CI conflicts
  - Increase timeouts to 1800s (30 min)
  - Add cleanupTimeoutSeconds
  - Add e2etest labels for tracking

  Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>


