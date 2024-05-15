# portainer

```bash
kubectl create namespace portainer
helm upgrade --install portainer portainer/portainer -f values.yaml -n portainer
```

```bash
sudo podman run -d   -p 9001:9001   --name portainer_agent   --restart=always   -v /run/podman/podman.sock:/var/run/docker.sock   -v /home/voidfork/.local/share/containers/storage/volumes:/var/lib/docker/volumes   portainer/agent:2.19.5

```