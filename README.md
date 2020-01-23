create_user
=========

Create a user and upload an ssh public key for remote authentication

Requirements
------------

Required to provide an ec2-user passed as an argument with the playbook command (i.e. -u ec2-user) 
Need  a dfault sshe public ssh key or a specific key needs to be called out in a variable

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.
#Define the user you would like to create
user_name: default
#Define the user state present or absent
user_state: present
#Define the path to the ssh public key
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

None

Example Playbook
----------------

---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/cloud_key.pub


License
-------

BSD

Author Information
------------------

Mohamed Ait
dayofmythology@gmail.com
