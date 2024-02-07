# KUBERNETES
## What is Kubernetes?

 * Kubernetes, often abbreviated as K8s
 * It is an open-source container orchestration platform.
 * It is designed to automate the deployment, scaling, and management of containerized applications.

## Why we use Kubernetes?

 * Kubernetes is a powerful tool for managing containerized applications in production environments.

 * Its features address many challenges associated with deploying and maintaining distributed systems

 * Key features of Kubernetes include:

Container Orchestration :
Automates deployment and management of containerized applications.

Scalability:
Dynamically scales applications based on demand for optimal resource use.

High Availability:
Ensures reliable application performance by distributing containers across nodes.

Portability:
Provides a consistent platform across diverse infrastructures and environments.

Resource Efficiency:
Optimizes resource allocation and scales applications based on utilization.

Service Discovery and Load Balancing:
Facilitates exposing and balancing traffic for applications.

Community and Ecosystem:
benefits from a large, active open-source community and extensive tooling.

Rolling Updates and Rollbacks:
Supports seamless application updates and automatic rollbacks.

Security and Compliance:
Implements features for securing applications and managing access.

Cost Savings:
contributes to savings through optimized resource use and automation.

## Architecture of Kubernetes
* Kubernetes Cluster mainly consists of a Control Plane and Worker Machines called Nodes

* It is also called as Master-Slave system

* We can create single or multiple master nodes for high availability and scalability.

* We also can create multiple slave nodes to handle worl load

* key components and architecture of Kubernetes:

API Server:

 * The API Server acts as the central management entity and the frontend interface for the Kubernetes control plane.
 * It processes RESTful requests to manage cluster resources and updates the corresponding objects in etcd.
 * It serves as the communication hub for other control plane components to interact and manage the cluster.

ETCD:

* etcd is a lightweight, distributed key-value store that securely and consistently stores the critical data of the Kubernetes cluster.
* It holds the cluster's configuration and state, including information about nodes, pods, configurations, secrets, and the state of workloads.

Scheduler:

* The Scheduler is responsible for assigning workloads, specifically pods, to appropriate nodes.
* It selects nodes for new pods based on resource requirements, quality of service requirements, affinity specifications, and other criteria.

Controller Manager:

* This component runs various controller processes in the background to regulate the state of the cluster and handle routine tasks.
* It helps in maintaining the desired state of the cluster.

kublet:

* The kubelet is responsible for executing commands that come from the Kubernetes control plane, including instructions from the scheduler.
* It communicates with the control plane and ensures that containers within pods are running as expected.

Kube-proxy:

* Kube-proxy maintains network rules on nodes, allowing communication between Pods.
* It handles network forwarding, load balancing, and service-related network tasks.

Container Engine:

* The container engine on a worker node is responsible for executing and managing containers.
* It provides the runtime environment for running containerized applications within the Kubernetes cluster, handling tasks such as container creation, start-up, and resource isolation.

POD:

* A Pod is the smallest deployable unit in Kubernetes.
* It's like wrapper around container.
* The worker node executes and hosts these Pods, running the specified containers within them.


## Lifecycle of kubernetes

* A user or application initiates a request to create a new pod.
* The API server, the central control point, communicates with ETCD, a persistent data store, to gather information about available nodes.
* The scheduler, responsible for pod placement, analyzes resource availability and constraints to choose the best node for the pod.
* The API server informs the kubelet, the agent running on the selected node, about the pod scheduling decision.
* The kubelet creates the pod's containers and manages its lifecycle on that node.
* The kubelet sends status updates back to the API server about the pod's progress.
* The API server stores the updated cluster state information in ETCD, ensuring a consistent view for all components.


## K8s Cluster - Minikube - Kind - Kubeadm - EKS - GKE - AKS - ...

* Kubectl Commands

Ref: https://www.bluematador.com/learn/kubectl-cheatsheet

   kubectl cluster-info    # to get cluster information
   kubectl api-resources   # to list available k8s objects
   kubectl api-version     # to list available api versions
   kubectl get nodes       # to get list of nodes
   kubectl get nodes -o wide   # to get IP of the nodes
   kubectl get pods        # to get list of pods
   kubectl get pods -o wide    # to get IP of the pods
 
INGRESS
* INGRESS: https://kubernetes.io/docs/concepts/services-networking/ingress/
* NGINX INGRESS CONTROLLER: https://docs.nginx.com/nginx-ingress-controller/installation/installing-nic/installation-with-manifests/
