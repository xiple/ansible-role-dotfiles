Ansible role: dotfiles
=========

[![CI](https://github.com/xiple/ansible-role-dotfiles/actions/workflows/ci.yml/badge.svg)](https://github.com/xiple/ansible-role-dotfiles/actions/workflows/ci.yml)

An ansible role that installs dotfiles. This role ensure `git` and `stow` package are installed.

Requirements
----------------

None.

Role Variables
----------------

Configure dotfiles repository location and local destination. Defaults are :

```yaml
dotfiles_repo_url: "https://github.com/xiple/dotfiles.git"
dotfiles_repo_version: main
dotfiles_repo_local_destination: "~/dotfiles"
```

Supported distributions
----------------

This role has been been developed and tested on the following distributions :

- Fedora 43
- Fedora 42

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - xiple.dotfiles
```

License
-------

MIT
