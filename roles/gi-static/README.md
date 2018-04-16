Role Name
=========

A brief description of the role goes here.

Requirements
------------


Ansible playbook to setup HTTPS using Let's encrypt on nginx.

The Ansible playbook installs everything needed to serve static files from a nginx server over HTTPS.
The server pass A rating on [SSL Labs](https://www.ssllabs.com/).

To use:

 1. Install [Ansible](https://www.ansible.com/)
 2. Setup an Ubuntu 16.04 server accessible over ssh
 3. Create `/etc/ansible/hosts` according to template below and change example.com to your domain
 4. Copy the rest of the files to an empty directory (`playbook.yml` in the root of that folder and the rest in the `templates` subfolder)
 5. Run `ansible-playbook playbook.yml`
 6. Copy your (static HTML) code to `/var/www/example.com` (`example.com` replaced with your domain)
 7. Restart nginx (`systemctl restart nginx`)


Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
