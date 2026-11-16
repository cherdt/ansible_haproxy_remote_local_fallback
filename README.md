Ansible HAProxy Remote with Local Fallback
=========

A work in progress. The goal is to have a repeatable deployment of HAProxy that loads content from one or more remote backend servers, but if they are not available fails over to a local server as a backup.

Requirements
------------

The local server would also need to be running a web server.

Role Variables
--------------

- remote_ip: the IP address of the remote web server
- remote_port: the port of the remote web server
- local_ip: the IP address of the local web server (127.0.0.1)
- local_port: the port of the local web server

Dependencies
------------

None so far.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

None selected yet!

Author Information
------------------

Blame cherdt.
