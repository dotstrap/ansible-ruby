ansible-ruby
============
[![Build Status](https://travis-ci.org/dotstrap/ansible-ruby.svg)](https://travis-ci.org/dotstrap/ansible-ruby)

Install & configure ruby; install extra gems.

Installation
------------

```
ansible-galaxy install dotstrap.ruby
```

Requirements
------------

A system package manager.

Role Variables
--------------

See [default variables] & [variables].

Dependencies
------------

None.

Example Playbook
----------------

Using all the [default variables]:

```
    - hosts: servers
      roles:
         - role: dotstrap.ruby
```

Overriding some of the [default variables]:

```
    - hosts: servers
      roles:
         - role: dotstrap.ruby
           install_state: latest
           configuration_state: present
           gem_home: "{{ ansible_user_dir }}/.gem"
           gems: 
             - thor
             - yard
             - travis

```

Notes
-----

__Warning__: This role modifies your default shell configuration file, eg.
`~/.bash_profile`, `~/.zshrc` or `~/.config/fish/config.fish`.

License
-------

MIT

Author Information
------------------

[@mwilliammyers]

[@mwilliammyers]: https://github.com/mwilliammyers
[aura]: https://github.com/aurapm/aura
[default variables]: defaults/main.yml
[dotstrap]: https://github.com/mwilliammyers/dotstrap
[fasd]: https://github.com/clvv/fasd
[files]: files/
[fish]: http://fishshell.com/
[homebrew]: https://github.com/Homebrew/homebrew
[variables]: vars/main.yml
[yaourt]: https://github.com/archlinuxfr/yaourt
[z]: https://github.com/rupa/z
[zsh]: http://zsh.sourceforge.net
