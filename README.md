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
           supervisord_programs:
             - name: django-uwsgi
               # directory to cwd to before exec (def no cwd)
               directory: "{{ project_home_path }}"
               command: "{{ site_virtualenv_path }}/bin/uwsgi --ini /etc/uwsgi/django-uwsgi.ini"
               # process environment additions (def no adds)
               environment: 'DJANGO_SETTINGS_MODULE="django_uwsgi.settings"'
               autostart: "true"
               autorestart: "true"
               stdout_logfile: "/var/log/supervisor/%(program_name)s.log"
               stdout_logfile_maxbytes: "2MB"
               stderr_logfile: "/var/log/supervisor/%(program_name)s.log"
               stderr_logfile_maxbytes: "2MB"
               stopsignal: "INT"
           supervisord_groups:
             - name: django-site
               programs: "django-uwsgi"

License
-------

MIT

Author Information
------------------

Maxim Avanov (https://maximavanov.com)
