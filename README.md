avanov.supervisord
==============================

Supervisord role for Ubuntu hosts

Install it with the following command:

```bash
$ ansible-galaxy install avanov.supervisord
```

Requirements
------------

None

Role Variables
--------------

Here is the list of all variables and their default values:

* ``supervisord_pip_path: /usr/bin/pip``
* ``supervisord_initscript_path: /etc/init.d/supervisor``
* ``supervisord_system_config_dir: /etc/supervisor``
* ``supervisord_system_config_path: "{{ supervisord_system_config_dir }}/supervisord.conf"``
* ``supervisord_supervisord_path: /usr/local/bin/supervisord``
* ``supervisord_supervisorctl_path: /usr/local/bin/supervisorctl``

Dependencies
------------

None

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - {role: avanov.supervisord }

License
-------

MIT

Author Information
------------------

Maxim Avanov (https://maximavanov.com)
