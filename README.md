# Fluentd role for ansible

Create `./library` directory in your ansible project:

```
mkdir ./library
```

And configure `ansible.cfg`:

```
[defaults]
roles_path = ./library
```

Add submodule:

```
git submodule add git@github.com:kressh/ansible-fluentd.git library/fluentd
```

Use role:

```yaml
---
- hosts: appservers
  remote_user: ansible
  become: true
  roles:
    - fluentd
```
