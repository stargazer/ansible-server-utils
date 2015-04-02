# ansible-server-utils

This Ansible role installs some common utilities on the server.

### Requirements

* A Debian machine running an SSH server and a user account with ``sudo`` permission

### Role Variables

* ``packages``: List of [packages](vars/main.yml). Override in order to specify specific versions or extra packages. When overriding, be aware that the initial value of packages doesn't hold anymore, so you need to specify all packages you'd like to install.

### Examples

    playbook.yml

    ---
    hosts: all
    remote_user: foo
    sudo: yes
    roles:
     - {role: 'ansible-server-utils'} 

Invoke playbook
    
    ansible-playbook playbook.yml

