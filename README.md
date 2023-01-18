pyenv
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.pyenv-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/pyenv)

Install [`pyenv`](https://github.com/pyenv/pyenv), a simple Python version manager. On macOS, installation is done via Homebrew. On Linux, the `pyenv` repository is cloned via `git`.

Requirements
------------

`git` installed
Homebrew installed on macOS.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `pyenv_repo_url` | `https://github.com/yyuu/pyenv.git` | URL used to clone via `git`. |
| `pyenv_repo_dest` | `{{ ansible_facts.user_dir }}/.pyenv` | Directory where `pyenv` will be cloned |
| `pyenv_user` | `root` | User account used to clone and configure `pyenv`. |
| `pyenv_shell` | `ansible_env.SHELL` | Shell used for setting up `pyenv`. Controls the lines inserted and into which shell config file. Supported shells are `fish`, `zsh`, and `bash`. |
| `pyenv_install_versions` | `[]` | List of Python versions to install. Must match a version in `pyenv install --list`. |

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      roles:
         - samdoran.pyenv

License
-------

Apache 2.0
