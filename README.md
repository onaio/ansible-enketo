Enketo
======

Use this role to setup [Enketo](https://enketo.org) behind [NGINX](https://nginx.org/en).
 
Role Dependencies
-----------------

 - [DavidWittman.redis](https://github.com/DavidWittman/ansible-redis)
 - [onaio.nvm](http://github.com/onaio/ansible-nvm)


Role Variables
--------------

Check [./defaults/main.yml](./defaults/main.yml) for default values for Ansible variables. Please ensure you provide values as strings (not booleans) for the following boolean variables:
- enketo_validate_page
- enketo_enable_offline
- enketo_managed_by_enketo
- enketo_allow_insecure_transport
- enketo_disable_save_drafts
- enketo_repeat_ordinals
- enketo_validate_continuously

Example Playbook
----------------

Playbook to setup Enketo might look like:

    - name: Setup Enketo
      hosts: enketo-servers
          enketo_api_salt: "some salt"
          enketo_api_token: "some token"
      roles:
        - role: enketo

License
-------

This project is released under the Apache 2 license. Read the [LICENSE.txt](./LICENSE.txt) file for more details.

Authors
-------

Update by [Ona Engineering](https://ona.io)
