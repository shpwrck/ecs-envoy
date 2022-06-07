## Expose ECS with TLS through an Istio Ingress Gateway on EKS

### Components

1. ECS -> host insecure apps
2. EKS -> host istio infrastructure
3. S3 -> host envoy configuration
4. Certificate Authorities -> secure communication

### Steps

1. Setup EKS Cluster 
1. Setup ECS Cluster with connectivity to EKS network
1. Setup S3 to host envoy config for tasks.
1. Create Task Definition and Service in ECS Cluster
1. Install Istio on EKS cluster
1. Deploy Istio configuration for ECS connectivity

### Gotchas

1. Network connectivity
2. Manual vs Automated Certificates
