# homelab-homepage

[Homepage](https://gethomepage.dev) deployment for the homelab k3s cluster, managed via ArgoCD.

A landing page of links to the other services in the cluster (Grafana, Pi-hole, OpenBao, Home Assistant, ArgoCD, Prometheus, Alertmanager). Accessible at `homelab.morrisons.site`.

Service links and external bookmarks (GitHub, Open PRs, Discord, etc.) are configured statically in `manifests/templates/configmap.yaml` (`services.yaml` and `bookmarks.yaml`) — no live status widgets or cluster/Docker API access is granted, so there's nothing here that needs credentials.

## Tests

```
make check
```

Runs the bats suite in `manifests/tests` against `helm template` output — no cluster required.

## CI

Pull requests run `mattjmorrison-homelab/actions-helm` (helm lint, `helm template`, and a server-side dry-run) via `.github/workflows/check.yml`. This is separate from `make check` — CI does not run the bats suite; that only runs locally.

---

[Homelab Docs](https://github.com/mattjmorrison/homelab/blob/main/docs/INDEX.md)
