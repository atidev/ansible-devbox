Role Name
=========

Role for setting up virtual box used for python web development.

Requirements
------------


Role Variables
--------------

```yaml
# default user for devbox
devbox_user: vagrant

# default group
devbox_group: vagrant

# update apt cache before installing packages
apt_update_cache: yes

# extra apt repos to install packages
apt_repos:
  - ppa:pi-rho/dev

# apt packages for installing
apt_packages:
  - unzip
  - git
  - mercurial
  - python-pip
  - python-dev
  - python3
  - python3-dev
  - supervisor
  - vim
  - nginx
  - tmux
  - rsync
  - ngrok-client

# python packages installed syste-mwide
pip_packages:
  - ansible
  - tox
  - nodeenv
  - devpi-web
  - devpi-server
  - httpie
  - ipython

# directory for local devpi cache
devpi_cache_dir: /srv/devpi

# port for nginx in dev mode
devbox_nginx_port: 8888

# root directory for webserver's static files
devbox_nginx_root: /srv/www/
```


Example Playbook
----------------

```yaml
- name: Devbox test playbook
  hosts: dev-vm
  vars:
    apt_update_cache: no
  roles:
    - devbox
```

License
-------

MIT

Author Information
------------------

Arthur Orlov

ati.su
