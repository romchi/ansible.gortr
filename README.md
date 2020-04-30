# Ansible role: gortr

Install and configure Cloudflare GoRTR on Debian/Ubuntu servers.

## Requirements

No requirements, install and use.


## Role Variables

There are only one dictionary variable with lot of settings (see `defaults/main.yml`):
    
    gortr: {}

All GoRTR settings in this dictionary variable, see descriptions in `defaults/main.yml`

_Note: If you use `hash_behaviour=replace` in your ansible.cnf, you need to replace all `gortr` variable or only needed parameters, otherwice variable will be overwriten._

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: rpkiserver
      vars:
        gortr:
          metrics.addr: "0.0.0.0:8081"

      roles:
         - { role: romchi.gortr, tags: gortr }

License
-------

MIT / BSD

Author Information
------------------

* [Roman Bulakh <bulah.roman@gmail.com>](https://github.com/romchi)
