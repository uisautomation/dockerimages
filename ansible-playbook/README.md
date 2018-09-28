# Ansible playbook

Packaged Ansible playbook with vault support.

Run via:

```bash
$ export VAULT_PASSWORD="some-password"
$ docker run \
    -t \
    -e VAULT_PASSWORD \
    -v ${SSH_AUTH_SOCK}:/ssh-agent -e SSH_AUTH_SOCK=/ssh-agent \
    -v $PWD:/workspace:ro \
    uisautomation/ansible-playbook:2.6 \
    <ansible-playbook options>...
```
