pyenv
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.pyenv-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/pyenv)
[![Build Status](https://travis-ci.org/samdoran/ansible-role-pyenv.svg?branch=master)](https://travis-ci.org/samdoran/ansible-role-pyenv)

Install [`pyenv`](https://github.com/pyenv/pyenv), simple Python version manager. On macOS, installation is done via Homebrew. On Linux, the `pyenv` repository is cloned via `git`.

Requirements
------------

`git` installed

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `pyenv_repo_url` | `https://github.com/yyuu/pyenv.git` | URL used to clone via `git`. |
| `pyenv_repo_dest` | `.pyenv` | Directory where `pyenv` will be cloned |
| `pyenv_chdir` | `{{ ansible_facts.user_dir }}` | Parent directory where  |


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

    - hosts: all
      roles:
         - samdoran.pyenv

License
-------

Apache 2.0
