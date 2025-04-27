# ACES ML Helm Charts Repository

This repository contains Helm charts for deploying the ACES ML service in Kubernetes environments.

## Available Charts

- **aces-ml-chart** (v1.0.1) - A Helm chart for deploying the ACES ML service with secure containerization and real-time model updates.

## Usage

### Adding the Repository

```bash
helm repo add aces-ml https://raw.githubusercontent.com/samirhimi/helm-charts/main
helm repo update
```

### Installing Charts

To install the ACES ML chart:

```bash
helm install aces-ml aces-ml/aces-ml-chart --version 1.0.1
```

## Chart Details

### aces-ml-chart

The ACES ML chart includes the following features:

- Secure containerization with non-root user settings
- Resource limits and requests configuration
- Horizontal Pod Autoscaling (HPA)
- Network policies for enhanced security
- Persistent volume support for dataset and model storage
- Configurable ingress settings
- Security context configurations

#### Default Configuration

- Image repository: aces-ml
- Image tag: 1.0.1
- Pull policy: Always
- Resource limits:
  - CPU: 1000m
  - Memory: 2Gi
- Resource requests:
  - CPU: 500m 
  - Memory: 1Gi
- Autoscaling enabled with 1-3 replicas
- Network policies enabled
- Persistent volumes for both dataset and model storage

For detailed configuration options, please refer to the chart's `values.yaml` file.

## Contributing

Please refer to our contribution guidelines for information on how to submit changes or new charts.

## License

This repository is licensed under the terms specified in the [LICENSE](LICENSE) file.