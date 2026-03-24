# Day 50 –Why was Kubernetes created? What problem does it solve that Docker alone cannot?

## Task 1: Recall the Kubernetes Story

Why was Kubernetes created? What problem does it solve that Docker alone cannot?
Who created Kubernetes and what was it inspired by?
What does the name "Kubernetes" mean?

### Why was Kubernetes created? What problem does it solve that Docker alone cannot?
Kubernetes solves scaling and restarting containers automatically, while earlier engineers had to do it manually.

so basically kubernetes was created to solve container orchestration problems such as

- scalling

- restarting

Managing containers across multiple machines

Docker helps to create and run containers, but when run many containers across many servers, Docker alone cannot easily manage them.

### Who created Kubernetes and what was it inspired by?

Kubernetes was created by Google in 2014.

It was inspired Borg tool which was automatically scalling and restarting the cantainer

later Google donates it to open-source

Today it is maintained by the Cloud Native Computing Foundation, which is part of the Linux Foundation.
And they named it as KUBERNETES

### What does the name "Kubernetes" mean?

Kubernetes comes from the Greek word meaning

Helmsman” or “Ship Pilot” (someone who steers a ship).

which means the cantainers are the ships and the steerign it is kubernetes

K8s is the short form of Kubernetes

There are 8 letters between K and S Kubernetes Architecture and Cluster Setup
From memory, draw or describe the Kubernetes architecture. Your diagram should include:

# Task 2: Draw the Kubernetes Architecture

Control Plane (Master Node):


API Server — the front door to the cluster, every command goes through it

etcd — the database that stores all cluster state

Scheduler — decides which node a new pod should run on

Controller Manager — watches the cluster and makes sure the desired state matches reality

Worker Node:

kubelet — the agent on each node that talks to the API server and manages pods

kube-proxy — handles networking rules so pods can communicate

Container Runtime — the engine that actually runs containers (containerd, CRI-O)

After drawing, verify your understanding:


### What happens when you run kubectl apply -f pod.yaml? Trace the request through each component.
- kubectl sends request to API Server
- API Server stores it in etcd
- Scheduler selects a node
- Kubelet starts the Pod on that node
- Container runs
### What happens if the API server goes down?

- kubectl will NOT work

- No new Pods can be created

- No updates, scaling, or changes

BUT:

- Already running Pods will keep running

  Why? Because worker nodes don’t need API server to keep containers running
  
 However:
 
- No healing
- No scheduling
- No monitoring updates
### What happens if a worker node goes down?
- Node becomes NotReady
- Pods on that node stop working 
- Kubernetes detects failure
- Pods are deleted and recreated on other nodes
- Application recovers automatically 

# Task 3: Install kubectl
kubectl is the CLI tool you will use to talk to your Kubernetes cluster.

Install it:
# Linux (amd64)
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
