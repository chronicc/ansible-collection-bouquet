Bouquet Stack
=============

Setup and manage bouquet stacks.

Requirements
------------

No specific requirements.

Role Variables
--------------

```yaml
# The directory where all bouquet stacks will be situated.
bouquet_root_dir: /srv/bouquet # noqa var-naming[no-role-prefix]

# A dictionary containing all stacks that will be deployed.
bouquet_stack_map: {}
  # bouquet_stack_map:
  #   webserver:
  #     services:
  #       nginx:
  #         image: nginx
  #         ports:
  #           - 80:80
  #           - 443:443
```

Dependencies
------------

- [geerlingguy.docker](https://github.com/geerlingguy/ansible-role-docker)

Example Playbook
----------------

    - hosts: servers
      pre_tasks:
        - name: Update apt cache
          ansible.builtin.apt:
            cache_valid_time: 3600
            update_cache: true
          when: ansible_os_family == 'Debian'
      roles:
        - role: bouquet_stack
      vars:
        bouquet_stack_map:
          webserver:
            services:
              nginx:
                image: nginx
                ports:
                  - 80:80
                  - 443:443

License
-------

MIT

Author Information
------------------

- chronicc <hello@chroni.cc>
