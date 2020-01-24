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

