# Kubernetes Showcase Project with Bazel - Structure

This document outlines the structure of the project repositories.

## Microservices Monorepo

```
microservices-monorepo/
├── WORKSPACE                    # Bazel workspace definition
├── BUILD.bazel                  # Root Bazel build file
├── .bazelrc                     # Bazel configuration
├── .github/workflows/           # GitHub Actions workflows
├── apps/                        # Application services
│   ├── order-api/               # Order service (Golang)
│   │   ├── BUILD.bazel          # Bazel build configuration
│   │   ├── cmd/                 # Command entrypoints
│   │   │   └── server/          # Server executable
│   │   │       ├── BUILD.bazel  # Bazel build configuration
│   │   │       └── main.go      # Main go file
│   │   └── pkg/                 # Internal packages
│   │       └── api/             # API implementation
│   │           └── BUILD.bazel  # Bazel build configuration
│   └── payment-api/             # Payment service (NestJS/TypeScript)
│       ├── BUILD.bazel          # Bazel build configuration
│       ├── src/                 # Source code
│       │   ├── main.ts          # Main entry point
│       │   ├── app.module.ts    # Main module
│       │   └── payments/        # Payments module
│       └── tsconfig.json        # TypeScript configuration
├── packages/                    # Shared libraries
│   ├── common/                  # Common utilities
│   │   └── BUILD.bazel          # Bazel build configuration
│   └── models/                  # Shared data models
│       └── BUILD.bazel          # Bazel build configuration
├── tools/                       # Development tools
│   ├── bazel/                   # Bazel-specific tools
│   │   └── rules/               # Custom Bazel rules
│   ├── docker/                  # Docker configuration
│   └── kind/                    # Kind cluster setup scripts
└── README.md                    # Project documentation
```

## Kubernetes Infrastructure

```
kubernetes-infra/
├── WORKSPACE                    # Bazel workspace for infrastructure
├── BUILD.bazel                  # Root Bazel build file
├── base/                        # Base Kubernetes manifests
│   ├── namespaces/              # Namespace definitions
│   ├── order-api/               # Order API base manifests
│   └── payment-api/             # Payment API base manifests
├── overlays/                    # Kustomize overlays
│   ├── development/             # Development environment
│   ├── staging/                 # Staging environment
│   └── production/              # Production environment
├── platform/                    # Platform components
│   ├── argocd/                  # ArgoCD configuration
│   ├── istio/                   # Istio service mesh
│   ├── karpenter/               # Karpenter autoscaler
│   ├── keyveron/                # Keyveron for secrets
│   ├── chaos-mesh/              # Chaos engineering
│   └── networking/              # Network policies
└── README.md                    # Infrastructure documentation
```