Create Users
=========
This role creates users on your Linux or UNIX server.


Requirements
------------

SSH access using PubKey Authentication.

Role Variables
--------------

username = the list of a single or multiple sudo enabled users to ensure on present on every targeted server.  

userpass = the password to set for each user created.  

The `userpass` var is stored in an encrypted file that is managed by `ansible-vault`.  To edit the file use `ansible-vault edit vars/passes.yml` with the password being set to `examplepassword`.  The password can be reset via `ansible-vault rekey vars/passes.yml`.

*note: for simplicity each user is created with the same example password which is a bad Linux/UNIX standard but works for this example playbook.  It is recommended that every user receives a unique strong password.*

Dependencies
------------

Python and Ansible installed on the control machine.

License
-------

GNU
