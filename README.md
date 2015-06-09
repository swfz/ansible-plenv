plenv
=========

ansible role to install plenv and set local and global version

Requirements
------------

require git and change settings able to git clone

Role Variables
--------------

* plenv_local

default is "5.18.2"

overwrite other vars file if you want to use other version

* plenv_global

default is "5.18.2"

overwrite other vars file if you want to use other version

* app_user

default is "vagrant"

username of application user

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - { role: swfz.plenv, app_user: "username", plenv_local_version: "5.20.2"}


* cron or daemon

use templates/env.j2 if use perl script with daemon and cron

* crontab

```
SCRIPT=/path/to/env
* * * * $SCRIPT plenv exec perl script.pl
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
