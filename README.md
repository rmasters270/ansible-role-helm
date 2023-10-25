# Helm

Install Helm, the package manager for Kubernetes.

[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-helm-blue.svg)](https://galaxy.ansible.com/ui/standalone/roles/rmasters270/helm)

## Role Variables

| Variable              | Required | Default                                                | Comments                                            |
| --------------------- | -------- | ------------------------------------------------------ | --------------------------------------------------- |
| helm_repo_certificate | yes      | <https://baltocdn.com/helm/signing.asc>                | Helm apt repository signing certificate             |
| helm_repo             | yes      | deb <https://baltocdn.com/helm/stable/debian> all main | Helm apt repository                                 |
| helm_diff_plugin_path | yes      | <https://github.com/databus23/helm-diff>               | Helm diff plugin URL                                |
| helm_repository       | no       |                                                        | Complex variable defining repository names and URLs |

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
