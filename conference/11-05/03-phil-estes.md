CRI Runtimes Deep Dive: Who's Running My Kubernetes Pod!?

PHIL ESTES

- kubelet -> dockershim -> dockerd
                        -> containerd
                        -> runc

- OCI (open container iniciative) specs
    - container runtimes
    - container registries

- CRI (container runtime interface)

- container runtime
    - pod container lifecycle
    - image mngmt
    - status
    - container interaction

- firecracker - amazon

why do change container runtime
- performance

- containerd as adapter between kubernetes and virtualization service



LINKS

https://github.com/containerd/cri
https://github.com/google/gvisor
https://thenewstack.io/how-to-implement-secure-containers-using-googles-gvisor/
