# tanzu-application-platform
A guided tutorial for setting up and experimenting with Tanzu Application Platform (TAP)

# Create a Kind Cluster

TAP can be installed on any type of kuberentes cluster, for this tutorial we will use Kind so that 

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

# Install the Tanzu cli 

1. Download the tanzu cli for your platform from [Tanzu Network](https://network.pivotal.io/products/tanzu-application-platform/#/releases/941562)
2. follow instructions in the [TAP docs](https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/0.1/tap-0-1/GUID-install.html#mac-cli)
 
 # Configure Tanzu CLI with TAP packages

 1. follow the instructions in [Add TAP repository](https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/0.1/tap-0-1/GUID-install.html#add-the-tap-package-repository-8)

 # Install Pre-reqs into K8s clustes

 1. Install kapp controller `kapp deploy -a kc -f kapp deploy -a kc -f https://github.com/vmware-tanzu/carvel-kapp-controller/releases/latest/download/release.yml`


2. Install flux `kapp deploy -a flux -f https://github.com/fluxcd/flux2/releases/download/v0.15.0/install.yaml`

 # Install Application accelerator 

 1. follow instructions in [Install Application Accelerator](https://docs.vmware.com/en/VMware-Tanzu-Application-Platform/0.1/tap-0-1/GUID-install.html#install-application-accelerator-11)