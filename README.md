Oh-My-ZSH
=========

Roll Oh-My-ZSH onto your laptop or server. A very simple role, but provides the necessary configuration for something that I love to use. By default, I use the
[Agnoster](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes#agnoster) theme in `defaults/main.yml`, which may require some fonts to be patched. You can find
a list of included themes [here](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes).

Requirements
------------

You will need to either set your default shell to ZSH, or install ZSH (Ubuntu 16.04 for example - `apt install zsh`) first.

Role Variables
--------------

The following variables are available:

```yml
username: "{{ lookup('env','USER')}}"   # this should be set by default. Check with $ env | grep USER.
zsh_theme: agnoster                     # set your preferred theme.
```

Dependencies
------------

None.

Example Playbook
----------------

The role can be included into your own plays by passing:

    - hosts: servers
      roles:
         - { role: xnoder.ansible-role-ohmyzsh }

License
-------

MIT

Author Information
------------------

Created by Paul Stevens | [@xnoder](https://github.com/xnoder) | [xnode.co.za](https://xnode.co.za)
