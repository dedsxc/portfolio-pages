# How to Run a Blockchain Node in Kubernetes? 🤔

Running a blockchain node in Kubernetes can help you achieve scalability, fault tolerance, and ease of management. This guide demonstrates how to deploy a blockchain node using a Kubernetes stack powered by ArgoCD, GitHub, and Helm.

The following tutorial will demonstrate how to deploy an [Ethereum](https://ethereum.org/) blockchain node on kubernetes cluster.

## Pre-requisite

- Kubernetes Cluster: Ensure you have a running Kubernetes cluster (e.g., managed services like EKS, AKS, GKE, or Minikube for local testing).
- ArgoCD: Set up ArgoCD for GitOps-based deployment. Install it in your cluster following ArgoCD installation steps.
- GitHub Repository: Host your Helm chart and application configurations in a GitHub repository.

## Build & Deploy Ethereum node

The ethereum client node software support many client. We will use [erigon](https://github.com/erigontech/erigon) which design for efficiency, better storage management

~~~python
print("hello pretty")
~~~