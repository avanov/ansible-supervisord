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

You can find a list of all available variables in ``defaults/main.yml``

Dependencies
------------

None

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - role: avanov.supervisord

License
-------

MIT

Author Information
------------------

Maxim Avanov (https://maximavanov.com)
