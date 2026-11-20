Ansible HAProxy Remote with Local Fallback
=========

A work in progress. The goal is to have a repeatable deployment of HAProxy that loads content from one or more remote backend servers, but if they are not available fails over to a local server as a backup.

Lightbulb moment! Why would I even need to do this? HAProxy delivers a 503 errorpage if no backend servers are available. I could just customize that to some extent. HAProxy claims you can "customize the HTTP error pages clients receive to add your own styling, text, and images" although I don't know that HAProxy can deliver any associated images. 

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

    - hosts: localhost
      roles:
        - role: haproxy_remote_local_fallback

Or

    ansible-playbook -i localhost, -K playbook.yml

License
-------

The Unlicense.

Author Information
------------------

Blame cherdt.
