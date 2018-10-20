ansible-role-goenv
==================

[![Build Status](https://travis-ci.org/bluk/ansible-role-goenv.svg?branch=master)](https://travis-ci.org/bluk/ansible-role-goenv)

An [Ansible][ansible] role to install [goenv][goenv].

Requirements
------------

1. Add `goenv` to your `$PATH` after install.

```
echo 'export PATH="$HOME/.goenv/bin:$PATH"' >> ~/.bash_profile
```

2. Run the following:

```
~/.goenv/bin/goenv init
```

Role Variables
--------------

* `goenv_install_path` - The path to install `goenv`.

* `goenv_git_url` - The git URL to clone `goenv` from.

* `goenv_git_update` - If the cloned `goenv` git repository should be updated.

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: bluk.goenv }
```

License
-------

[Apache-2.0][license]

[license]: LICENSE
[ansible]: https://www.ansible.com
[goenv]: https://github.com/syndbg/goenv
