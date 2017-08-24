service-account
=========

This role creates a system group and user for other roles.

Requirements
------------

None

Role Variables
--------------

The variable `service_account_opts` is merged over the `service_account_defaults` variable.
Required variables are:

    service_account_opts:
      user:
      group:

Dependencies
------------

None

Example Playbook
----------------

    dependencies:
      -
        src: https://github.com/jnbnyc/ansible-role-service-account.git
        name: service-account
        service_account_opts:
          user: "{{ ansible_user }}"
          group: "{{ ansible_group }}"
          groups: ["sudo", "admin"]
          comment: "Ansible Client User"

License
-------

MIT

Author Information
------------------

jnbuhaynyc@gmail.com
