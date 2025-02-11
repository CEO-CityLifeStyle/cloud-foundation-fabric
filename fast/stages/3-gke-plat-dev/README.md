# GKE Development Environment

This stage deploys the GKE development environment in the me-central2 (Dammam) region, following CityLifeStyle's regional strategy.

## Configuration

1. Copy `terraform.tfvars.example` to `terraform.tfvars`
2. Update the following values in your `terraform.tfvars`:
   - `billing_account`: Your GCP billing account ID
   - `folder_ids`: Your GCP folder IDs
   - VPC configurations to match your network setup
   - Adjust cluster configurations as needed

## Regional Strategy
- Primary Region: me-central2 (Dammam, KSA)
- All workloads and data storage components are deployed in me-central2
- Ensures KSA data residency compliance

## GKE Cluster Configuration
The GKE cluster is configured with:
- Workload Identity enabled
- GKE Dataplane V2
- Cluster autoscaling with defined resource limits
- Enhanced logging and monitoring
- Integration with shared VPC

## Security Features
- Private GKE cluster
- Workload Identity for secure service account management
- Network policies enabled
- Regular security updates through node auto-upgrade

## Monitoring and Logging
- System and workload logging enabled
- Managed Prometheus for monitoring
- Custom metrics collection
- Integration with Cloud Monitoring

## Network Configuration
- Integrated with shared VPC
- Secure network policies
- Private cluster configuration
