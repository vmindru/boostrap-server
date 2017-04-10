bootstrap-server
=========

Boostrap server with 

  - enable firewall
  - enable selinux 
  - create users and propagate SSH keys
  - grant sudo access for trusted users
  - lock root user 
  - install basic RPM files



Role Variables
--------------

    boostrap_users:                     # list of users to add to the server
    boostrap_enable_firewall: True      # Make sure firewall is enabled allowing only SSH access
    boostratp_enable_selinux: True      # Make sure selinux is enabled
    bootsrap_sudo: True                 # grant sudo access to boostrap_users
    bootsrap_lock_roouser: True         # Lock direct root user access
    bootstrap_basic_rpm:  list          # List of rpm files to install


Dependencies
------------

none


Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: boostrap-server }

License
-------

GNU GPLv3


Author Information
------------------

vmindru@redhat.com
