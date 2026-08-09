# homelab-homepage

[Homepage](https://gethomepage.dev) deployment for the homelab k3s cluster, managed via ArgoCD.

A landing page of links to the other services in the cluster (Grafana, Pi-hole, OpenBao, Home Assistant, ArgoCD, Prometheus, Alertmanager). Accessible at `homelab.morrisons.site`.

Service links are configured statically in `manifests/configmap.yaml` (`services.yaml`) — no live status widgets or cluster/Docker API access is granted, so there's nothing here that needs credentials.

---

[Homelab Docs](https://github.com/mattjmorrison/homelab/blob/main/docs/INDEX.md)
