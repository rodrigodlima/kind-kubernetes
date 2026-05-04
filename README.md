# kind-kubernetes

## Run kind with Podman

### First, install Podman

```
podman machine stop
podman machine rm
podman machine init --rootful
podman machine start
```

### Set Docker socket to use Podman

```
export DOCKER_HOST=unix://$HOME/.local/share/containers/podman/machine/podman.sock
```
Put this in your .zshrc or .bashrc file too

### Create kind cluster

kind create cluster --config=kind-config.yaml
