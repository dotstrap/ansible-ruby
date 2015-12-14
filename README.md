dotstrap-ruby
=========
[![Build Status](https://travis-ci.org/mkwmms/ansible-dotstrap-ruby.svg)](https://travis-ci.org/mkwmms/ansible-dotstrap-ruby)

Bootstrap ruby: install ruby, configure dotfiles, & install extra gems.

Requirements
------------

None.

Role Variables
--------------

See [default variables].

Dependencies
------------

None.

Example Playbook
----------------

Using all the [default variables]:

```
    - hosts: servers
      roles:
         - role: mkwmms.dotstrap-ruby
```

Overriding some of the [default variables]:

```
    - hosts: servers
      roles:
         - role: mkwmms.dotstrap-ruby
           install_state: latest
           configuration_state: present
           gem_home: "{{ ansible_user_dir }}/.gem"
           gems: 
             - thor
             - yard
             - travis

```

License
-------

GPLv3

Author Information
------------------

[@mkwmms]

[@mkwmms]: https://github.com/mkwmms
[files]: files/
[default variables]: defaults/main.yml
[variables]: vars/main.yml
