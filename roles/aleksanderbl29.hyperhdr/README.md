Ansible Role HyperHDR
=========

[![CI](https://github.com/aleksanderbl29/ansible-role-hyperhdr/actions/workflows/ci.yml/badge.svg)](https://github.com/aleksanderbl29/ansible-role-hyperhdr/actions/workflows/ci.yml)

A role to deploy HyperHDR on debian based systems.

Is tested on Ubuntu 2204 and 2404 and Debian 11 and 12 through molecule. I use it in my environment with RpiOS based on Debian 11.

Requirements
------------

None

Role Variables
--------------

None for now

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
        - aleksanderbl29.hyperhdr

License
-------

GPL v3

Author Information
------------------

This role was created in 2024 by [Aleksander Bang-Larsen](https://github.com/aleksanderbl29)
