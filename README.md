# Reuseable Repository for ***GatewayApi*** into **Staging** and **Development** Environment

This workflow is reference from **airborneo-cms** repo so that compatiable with variables.

1. Input environment function

2. Install OCI CLI

3. Set up kubectl

4. Set up Kustomize

5. Configure Oracle Cloud and Kubernetes access

6. Verify cluster connection

## Workflow file

- `.github/workflows/install-gateway.yaml`

## What actions in this workflow

1. Check **gatewayclass** and **gateway** in *nginx-gateway* namespace.

2. If these are already installed, skip these steps and go to step **4**.

3. If there are not installed yet, will install the following steps.
   1. Gateway API CRDs
   2. Gateway Class

4. Install **gateway** in *nginx-gateway* namespace.

    
# What in this Repository

- We will use **Kustomization** method to patch depend on what we require for   two environments **Development** and **Staging**.

- Install Nginx Gateway Fabric
  - Reference: [Nginx Gateway Fabric][gatewayclass]

[gatewayclass]: https://docs.nginx.com/nginx-gateway-fabric/install/helm/

- Install Gateway-api
  - Reference: [Gateway-Api]

[Gateway-Api]: https://gateway-api.sigs.k8s.io/