# KUBERNETES

## What is Kubernetes?
ANS: 
   
    1) Google Cloud is the birthplace of Kubernetes—originally developed at Google and released as open source in 2014.  Kubernetes builds on 15 years of running Google's containerized workloads and the valuable contributions from the open source community. Inspired by Google’s internal cluster management system, Borg, Kubernetes makes everything associated    with deploying and managing your application easier.]

    2)Kubernetes (sometimes shortened to K8s with the 8 standing for the number of letters between the “K” and the “s”) is an open source system to deploy, scale, and manage containerized applications anywhere.

    3)Kubernetes, often referred to as K8s, is an open-source platform for managing containerized workloads and services.
      . It is a portable, extensible, and extensible system that facilitates both declarative configuration and automation.
      . Kubernetes was developed at Google and has since become the de facto standard for deploying and operating containerized applications.
      
    4)Providing automated container orchestration, Kubernetes improves your reliability and reduces the time and resources attributed to daily operations.


## why we use kubernets?
ANS: 
    1)Kubernetes is used for a variety of reasons, including reliability, scalability, security, cost optimization, and  faster time to market. It automates the deployment, scaling, and management of containerized applications, making it easier to deploy and manage applications, scale them as needed, and ensure their reliability and security.

    2)Kubernetes also helps in optimizing IT costs by efficiently managing container orchestration and allowing for better resource utilization.

    3) Additionally, it provides multi-cloud flexibility, making it easier to run applications on any public cloud service or a combination of public and private clouds, thus avoiding vendor lock-in.

    4)Furthermore, Kubernetes can help in achieving faster time to market by providing a portable, extensible, open-source platform for managing containerized workloads and services.

    Here are some key reasons why organizations choose to use Kubernetes:
    1)Container Orchestration
    2)Scalability
    3)High Availability
    4)Portability
    5)Rolling Updates and Rollbacks
    6)Resource Efficiency
    7)auto-healing & auto restart
    8)auto-scaling
    9)load balancing
    10)security management

## Architecture of Kubernetes
ANS: https://media.geeksforgeeks.org/wp-content/uploads/20190904034023/Docker2-1-1024x439.png

     The architecture of Kubernetes is designed to provide a scalable and extensible platform for deploying, managing, and orchestrating containerized applications.

     1)Cluster:A cluster is a set of nodes grouped together to run containerized applications. The cluster is the foundation of the Kubernetes architecture.

     2)Node:A node is a physical or virtual machine that runs containerized applications. Each node in the cluster runs a container runtime (such as Docker) to manage containers.

     3)Master Node:The master node is responsible for managing the cluster and making global decisions about the cluster (e.g., scheduling), as well as detecting and responding to cluster events (e.g., starting up a new pod when a deployment's replicas field is unsatisfied).
       Key components on the master node include:
       * API Server: Exposes the Kubernetes API, which is used by users and other components.
                     all the communication happens inside the cluster is with help of API'S.
       * Controller Manager: Manages controller processes that regulate the state of the system.
                     Controller Manger responsible to maintaing actual state and desire state.it manages all the 
                     controller in kubernet.
       * Scheduler: Assigns nodes to newly created pods based on resource requirements and constraints.
                    Scheduler is responsible to schedule commands on particular worker node.
       * etcd:etcd is a distributed key-value store that stores the configuration data of the cluster. It is used by the master components to store and retrieve configuration data, and it ensures high availability.

    4)Kubelet:The kubelet is an agent that runs on each node in the cluster. It is responsible for making sure that containers are running in a pod.
    It communicates with the master node components, receives instructions on which pods and containers to run, and ensures their proper execution.

    5)Kube-proxy:Kube-proxy maintains network rules on nodes. It enables communication across the cluster, handles load balancing for services, and performs network address translation (NAT) for service exposure.
      Allow network communiction inside the cluster. 

    6)Pod:A pod is the smallest deployable unit in Kubernetes and represents a single instance of a running process in a cluster. It can contain one or more containers that share the same network namespace, storage, and can communicate with each other.

    7)Service:A service defines a set of pods and a policy to access them. It provides a stable endpoint (IP address and DNS name) to access the pods, enabling load balancing and service discovery.

## Lifecycle of kubernetes
ANS: 

    In the Kubernetes request flow, a user initiates a request, and their kubeconfig file is used for authentication against the Kubernetes API server. The API server --> acting as the control plane's entry point-->  validates and processes requests --> interacting with the etcd key-value store to manage cluster state.

    * The Controller Manager and Scheduler ensure the desired state is maintained by assigning workloads to nodes.
 
    * The Kubelet on each node communicates with the API server, while the container runtime pulls and runs containers.  Networking and optionally, load balancing mechanisms facilitate communication between pods and services. 

    * Monitoring and logging tools capture relevant data, and the results of the user's request are then communicated back, completing the request flow.


