Atop
====

Ansible role to install and configure Atop.

Requirements
------------

No requirements.

Role Variables
--------------

| Variable               | Default         | Description                                                       |
| ---------------------- | --------------- | ----------------------------------------------------------------- |
| `atop_enable_daemon`   | `true`          | Run `atop` as a daemon                                            |
| `atop_enable_rotation` | `true`          | Use the `atop-rotate.timer` to support daily log files            |
| `atop_enable_pacct`    | `true`          | Support handling of terminated processes using process accounting |
| `atop_logopts`         | `""`            | Used to specify specific log options                              |
| `atop_loginterval`     | `600`           | Log interval in seconds                                           |
| `atop_loggenerations`  | `28`            | How many log files should be kept                                 |
| `atop_logpath`         | `/var/log/atop` | The path where atop should create its logfiles                    |

Dependencies
------------

No dependencies.

Tested operating systems
------------------------

This role was tested on RHEL8 and Debian versions 11 and 12.

Example Playbook
----------------

    - hosts: all
      roles:
         - role: atop
           tags: ['atop']

License
-------

MIT

Author Information
------------------

* Chris van Meer <c.v.meer@atcomputing.nl>
