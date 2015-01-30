lsyncd-cluster
=========

Installs and configures a set of lsyncd installations on different hosts and assings 1 host to be the master

Requirements
------------

None

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

  - lsyncd_max_user_watches: 4194304
    - Desired number of inotify watches in the kernel. Should be more then the number of files and folders you want to be kept in sync
    
  - lsyncd_path: /data
    - The folder you want to keep in sync

  - lsyncd_master_node: -1a-
    - This is a part of, or the complete hostname that you want to assing as the "master" lsyncd
    
  - play_hosts
    - Built-in variable containing all the hosts in the current play that this role finds itself in.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: markmaas.ansible-lsyncd-cluster }

License
-------

GPLv3

Author Information
------------------

Mark Maas
mark@maas-martin.nl
Fastest way to my heart is via email
