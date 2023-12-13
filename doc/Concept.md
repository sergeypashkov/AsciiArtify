**Introduction**

1.  **minikube**
minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.
All you need is a Docker (or similarly compatible) container or a Virtual Machine environment.

2.  **kind**
kind is a tool for running local Kubernetes clusters using Docker container “nodes”.
kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI.
**NOTE**: kind is still a work in progress

3.  **k3d**
k3d is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.
k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes.

**Characteristics**
| |**minikube**|**kind**|**k3d**|
|--|--|--|--|
|**Supported OS and archs**  |Linux (x86-64 ARM64 ARMv7 ppc64 s390x), macOS (x86-64 ARM64), Windows (x86-64)|Linux (x86-64 ARM64), macOS (x86-64 ARM64), Windows (x86-64)|Linux (x86-64 ARM64), macOS (x86-64 ARM64), Windows (x86-64)|
|**Monitoring**|Dashboard|||

[<img alt="alt_text" width="800px" src="hello.gif" />]
