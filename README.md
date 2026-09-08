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

Configure dotfiles backup. Defaults are :

```yaml
dotfiles_backup_dir: "~/dotfiles_backup"
dotfiles_to_backup:
  - .bashrc
  - .bash_profile
  - .bash_logout
```

In case you don't want backup :

```yaml
dotfiles_manage_backup: true
```

Supported distributions
----------------

This role has been developed and tested mainly for Fedora 44. Due to its simplicity, it should also work on other Linux distribution.

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
