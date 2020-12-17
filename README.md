# OPA Gatekeeper Playground

Creating an admin account on argocd manually:
```
  rbacConfig:
    # policy.default: role:readonly
    policy.csv: |
        p, role:org-admin, applications, *, */*, allow
        p, role:org-admin, clusters, get, *, allow
        p, role:org-admin, repositories, get, *, allow
        p, role:org-admin, repositories, create, *, allow
        p, role:org-admin, repositories, update, *, allow
        p, role:org-admin, repositories, delete, *, allow

        g, poc, role:org-admin
  config:
    # users.anonymous.enabled: "true"
    accounts.poc: apiKey, login


```
