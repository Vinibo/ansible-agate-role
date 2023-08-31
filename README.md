Ansible Agate
=========

This role deploy the Agate Gemini Server (https://github.com/mbrubeck/agate) on x86 or ARM Linux computers.

Requirements
------------

None

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):
```yaml
agate_port: 1965
agate_root_folder: "/srv/gemini"
agate_root_domain: ""
```

- `agate_port`: Default value 1965. Port on which Agate will listen
- `agate_root_folder`: Default value "/srv/gemini". Location of the files to serve by Agate. The folder will be created.
- `agate_root_domain`: No default value. Should be set to the domain that will serve the Gemini capsule. This value will be used by Agate to generate its SSL certificate.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: vinibo.ansible-agate, agate_domain: "geminispace.info" }

License
-------

MIT
