# tanzu-application-platform
A guided tutorial for setting up and experimenting with Tanzu Application Platform (TAP)

# Create a Kind Cluster

1. Inspect the contents of `k8s-kind-cluster.yml` it defines the kuberentes cluster that will be launched by kind
1. run the command `kind create cluster --config k8s-kind-cluster.yml` you will see output similar to the one below

```text
Creating cluster "tap-cluster" ...
 ✓ Ensuring node image (kindest/node:v1.19.11) 🖼 
 ✓ Preparing nodes 📦 📦 📦 📦  
 ✓ Writing configuration 📜 
 ✓ Starting control-plane 🕹️ 
 ✓ Installing CNI 🔌 
 ✓ Installing StorageClass 💾 
 ✓ Joining worker nodes 🚜 
Set kubectl context to "kind-tap-cluster"
You can now use your cluster with:

kubectl cluster-info --context kind-tap-cluster

Not sure what to do next? 😅  Check out https://kind.sigs.k8s.io/docs/user/quick-start/
```