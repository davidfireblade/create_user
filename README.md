create_user
=========

Create a user and upload an ssh public key for a remote authentication

Requirements
------------

No specific required Ansible
Need a default ssh public ssh public or a specific key needs to be called out in a variable

Role Variables
--------------

#Define the user you would like to create
user_name: default
#Define the user state present or absent
user_state: present
#Define the path to the ssh public key
ssh_key: ~/.ssh/is_rsa.pub

Dependencies
------------

None

Example Playbook
----------------

--
- hosts: all
  become: yes
  become_method: sudo
  become_user: root
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/cloud_key.pub

License
-------

MIT

Author Information
------------------

dsalinasvila@gmail.com
