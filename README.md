# Helm

Install Helm, the package manager for Kubernetes.

## Role Variables

### helm _repository

When this optional variable is defined it will add and update the respective Helm repositories.

```yaml
helm_repository:
  name: jetstack
    url: https://charts.jetstack.io
  name: traefik
    url: https://helm.traefik.io/traefik
  name: rancher-stable
    url: https://releases.rancher.com/server-charts/stable
```

## Example Playbook

```yaml
- hosts: localhost

  roles:
    - rmasters270.helm
```

## License

MIT

## Author Information

Ryan Masters
