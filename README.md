[![Build Status](https://travis-ci.com/ned300889/apache.svg?branch=master)](https://travis-ci.com/ned300889/apache) [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

Role Name
=========
Apache role


Role Variables
--------------
Following variables can be set at the playbook level, currently defined in defaults.yml

    disable_defaults: True

Disable default site, only applicable to Ubuntu

    self_signed: True
    ssl_path: "/etc/ssl/{{ site_name }}"

Generates a self signed certificate, disable to provide your own certificate


    make_dummy_site: True


Dependecies
----------------

None

Example Playbook
----------------


    - hosts: all
      vars_file: vars/main.yml
      roles:
         - { role: ned300889.apache }

Inside vars/main.yml

    disable_defaults: true
    self_signed: True
    site_name: example.com

License
-------

MIT / GPL v3

Author Information
------------------

Nathan Simpson.
