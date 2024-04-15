# DevOps-AsciiArtify

## Comparative Analysis

| Tools            | Minikube                                     | KIND                                           | k3d                                          |
|------------------|--------------------------------------------|-----------------------------------------------|----------------------------------------------|
| Description      | Local Kubernetes system for deploying Kubernetes clusters on a single machine | Allows creating local Kubernetes clusters in Docker containers | Tool for creating local Kubernetes clusters in Docker containers using Rancher Kubernetes Engine (RKE) |
| Supported OS     | + Linux, macOS, Windows                    | + Linux, Windows - macOS                     | + Linux, macOS - Windows                    |
| Supported Architectures | + x86, x86_64, ARM64                    | + x86, x86_64, ARM64                         | + x86, x86_64, ARM64                        |
| Automation       | + Provides a certain level of automation   | - Lack of built-in automation tools           | + Ability to automate deployment and cluster management through scripts and scenarios |
| Additional Features | + Monitoring, cluster management          | - No built-in monitoring and management tools | - Limited functionality                     |
| Ease of Setup and Use | - Not as user-friendly                   | + Easy to use                                 | + Simple and intuitive interface            |
| Deployment Speed | - Requires time for image loading         | + High deployment speed                       | + Fast deployment due to Docker container usage |
| Stability        | + Stable                                   | + High stability                               | + Stable                                    |
| Documentation and Support | + High-quality documentation and support | + High-quality documentation and support      | + Quality documentation and community support |

## Conclusions

Upon reviewing the three tools for deploying a local Kubernetes cluster for the "AsciiArtify" startup PoC, it was found that each has its own advantages and disadvantages. After evaluating various parameters, I recommend using k3d for deploying local Kubernetes clusters in your PoC projects. It boasts high ease of use, deployment speed, and stability, which are crucial for quickly starting your product development.

## Demonstration

You can familiarize yourself with the process of deploying a Kubernetes cluster using k3d [here](.doc/k3d.md).

[link to video](https://asciinema.org/a/XdYsLpd0n2F46dEzziceor0R8)

![demonstration](./assets/demo.gif)
