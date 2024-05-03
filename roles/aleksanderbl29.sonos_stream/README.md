# ansible-role-sonos-stream

[![CI](https://github.com/aleksanderbl29/ansible-role-sonos-stream/actions/workflows/ci.yml/badge.svg)](https://github.com/aleksanderbl29/ansible-role-sonos-stream/actions/workflows/ci.yml)

Ansible Role to deploy local Sonos radio for vinyl streaming on Debian/Ubuntu/Raspbian

CURRENTLY A WORK IN PROGRESS - DO NOT DEPLOY

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Disable service verification with the following variables.
Set `disable_verification` to disable all verification after installation and launch.
Set `disable_conn_validation` to not check if the service is reachable
Set `disable_stream_endpoint_check` to not check if the configured stream endpoint is reachable

The defaults (verification turned on) is false for all three. None of the variables are required for deployment.

    - disable_verification: false
    - disable_conn_validation: false
    - disable_stream_endpoint_check: false

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: aleksanderbl29.sonos_stream
          disable_verification: false

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
