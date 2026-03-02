# Hanzo Fi Payment Helm Charts

Kubernetes deployment charts for the Hanzo Fi Payment Switch and related services.

## Components

- **payment-switch** — Core payment routing engine
- **control-center** — Web dashboard
- **card-vault** — PCI-compliant card tokenization

## Quick Start

```bash
helm repo add hanzofi https://hanzofi.github.io/payment-helm
helm install payments hanzofi/hanzo-payments --namespace payments --create-namespace
```

## Configuration

```yaml
# values.yaml
server:
  replicas: 3
  resources:
    requests:
      cpu: 500m
      memory: 512Mi

database:
  host: postgres.svc
  name: payments

redis:
  host: redis.svc
```

## License

Apache 2.0 — see [LICENSE](LICENSE)

