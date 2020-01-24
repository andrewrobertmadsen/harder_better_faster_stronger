# Getting Started With Minikube

## Installation

Follow this setup tutorial:

https://kubernetes.io/blog/2019/03/28/running-kubernetes-locally-on-linux-with-minikube-now-with-kubernetes-1.14-support/

You might need to run:

```sudo chown -R your_username:libvirt /var/run/libvirt```

if you see the error
```Unable to start VM. Please investigate and run 'minikube delete' if possible
❌  Error: [KVM2_NO_DOMAIN] Error getting state for host: getting connection: looking up domain: virError(Code=42, Domain=10, Message='Domain not found: no domain with matching name 'minikube'')
💡  Suggestion: The VM that minikube is configured for no longer exists. Run 'minikube delete'
⁉️   Related issues:
    ▪ https://github.com/kubernetes/minikube/issues/3636
```

## Running Minikube

You can run minikube on kvm2 one of two ways:

Specifying minikube each time:

```minikube start --vm-driver kvm2```

Or by setting kvm2 as the default:

```
minikube config set vm-driver kvm2
minikube start
```

Some needed deps will be downloaded and then you should see something like:

```buildoutcfg
Waiting for cluster to come online ...
🏄Done! kubectl is now configured to use "minikube"
```

To validate that a k8s cluster is up, you can run:

```kubectl get nodes```

## Running something directly from a dockerhub image:

Create a nginx deployment.

```kubectl create deployment nginx --image=nginx```

Tear down the deployment
```buildoutcfg
kubectl delete deployment nginx
```
