dotstrap-ruby
=========
[![Build Status](https://travis-ci.org/mkwmms/ansible-dotstrap-ruby.svg)](https://travis-ci.org/mkwmms/ansible-dotstrap-ruby)<Paste>

Bootstrap ruby: install ruby & configure dotfiles, install extra gems.

Requirements
------------

None.

Role Variables
--------------

The following `gem` packages will be installed:

```
packages: 
  - thor
  - colorize
  - chronic
  - dotstrap
  - jeweler
  - docopt
  - ghi
  - yard
  - travis
  - tmuxinator
  - parallel
  - bundler
```

The following configuration files will be used:

`files/path.sh` for `zsh`, `bash`, & `sh` shells.

`files/path.fish` for `fish` shell.

Dependencies
------------

```
mkwmms.dotstrap
```

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - { role: mkwmms.dotstrap-ruby }
```

License
-------

GPLv3

Author Information
------------------

[@mkwmms]

[@mkwmms]: https://github.com/mkwmms
