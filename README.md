# Kubernetes Showcase Project with Bazel

This project demonstrates various Kubernetes features using a microservices architecture with Bazel as the build system, deployed with Kind/Minikube and managed with modern DevOps practices.

## Features Demonstrated

- **Bazel Build System**: Fast and reproducible builds for the entire monorepo
- **Microservices Architecture**: Order API (Go) and Payment API (NestJS/TypeScript)
- **Kubernetes Features**:
  - **Kustomize**: Environment-specific configurations
  - **Karpenter**: Auto-scaling for efficient resource management
  - **Chaos Engineering**: Testing resilience with Chaos Mesh
  - **Network Policies**: Secure communication between services
  - **Istio**: Service mesh for traffic management and observability
  - **KeyVeron**: Secure secrets management
  - **ArgoCD**: GitOps-based continuous deployment

## Getting Started

To get started, follow these steps:

1. Clone this repository
2. Set up a local Kubernetes cluster with Kind or Minikube
3. Build the applications with Bazel
4. Deploy to Kubernetes

Detailed instructions can be found in the documentation.

## License

This project is licensed under the MIT License.