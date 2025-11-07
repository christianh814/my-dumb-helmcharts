# Example App

A simple example Helm chart to demonstrate the structure.

## Installation

```bash
helm install my-example-app my-charts/example-app
```

## Configuration

The following table lists the configurable parameters:

| Parameter | Description | Default |
|-----------|-------------|---------|
| `replicaCount` | Number of replicas | `1` |
| `image.repository` | Image repository | `nginx` |
| `image.tag` | Image tag | `1.25` |
| `service.type` | Service type | `ClusterIP` |
| `service.port` | Service port | `80` |
