Create User
=========

Create a user and upload an SSH pub key for remote auth

Requirements
------------

No Specific required Ansible
Need a default SSH public key defined or changed

Role Variables
--------------

#Define the user you would like to create
user_name: default
# Define the user state present or absent
user_state: present
# Define the path to the SSH key
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------


Example Playbook
----------------

---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/id_rsa.pub


License
-------

MIT

Author Information
------------------

eugene@webhostingzone.org
