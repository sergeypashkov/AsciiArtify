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
|**Monitoring**|Dashboard|External|External|
|**Multi-node**|+|+|+|
|**IPv6**|-|+|+|

**Pros&Cons**

1.  **minikube**

Pros:
  * A lot of addons and drivers
  * Deploys Kubernetes as a container, VM or bare-metal
  * Dashboard that allows you to view and manage your cluster from a web browser.

Cons:
  * Not for production
  * Slow startup

2.  **kind**
   
Pros:
  * Very fast

Cons:
  * Still in development
  * Lack of documentation
  * No dashboard

3.  **k3d**
   
   Pros:
  * Very fast
  * Based on k3s, easier to switch to the production environment

Cons:
  * No dashboard

**Demonstration**

[<img alt="alt_text" width="800px" src="hello.gif" />]

**Summary**

I recommend k3d as a mature product which is based on a fast k3s engine
