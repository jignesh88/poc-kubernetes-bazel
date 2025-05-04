
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

## Repository Structure

This project consists of two repositories:

1. **Microservices Monorepo**: Application code and CI pipeline with Bazel
   ```
   microservices-monorepo/
   ├── WORKSPACE            # Bazel workspace definition
   ├── BUILD.bazel          # Root Bazel build file
   ├── .bazelrc             # Bazel configuration
   ├── .github/workflows/   # GitHub Actions pipelines
   ├── apps/                # Application services
   │   ├── order-api/       # Order service (Golang)
   │   └── payment-api/     # Payment service (NestJS)
   ├── packages/            # Shared libraries
   ├── tools/               # Development tools
   └── ...
   ```

2. **Kubernetes Infrastructure**: Kubernetes manifests and configurations
   ```
   kubernetes-infra/
   ├── WORKSPACE            # Bazel workspace for infrastructure
   ├── BUILD.bazel          # Root Bazel build file
   ├── base/                # Base Kubernetes manifests
   ├── overlays/            # Kustomize overlays for environments
   ├── platform/            # Platform components
   └── ...
   ```

## Getting Started

See the [detailed setup instructions](docs/minikube-bazel-instructions.md) for how to run this project with Minikube.

For a quick start with Kind, check the [Kind setup instructions](docs/kind-setup.md).

## Working with Bazel

See the [Bazel usage guide](docs/bazel-usage.md) for detailed instructions on working with Bazel in this project.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
