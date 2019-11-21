# jpartain89.install_monit_from_source

| **Travis-CI** |
| ------------ |
| [![Build Status](https://travis-ci.com/jpartain89/ansible-role-install-monit-from-source.svg?branch=master)](https://travis-ci.com/jpartain89/ansible-role-install-monit-from-source) |

Installation of Monit from their [Git Repo](https://bitbucket.org/tildeslash/monit)

## Role Variables

There are two sets of variable files I use in this role, one in the `defaults` directory (which contains the variables that are the easiest for you to override) and a debian.yml file in the `vars` directory, which are "stickier" variables, so-to-speak (these are usually best left alone).

Here is a list of the variables in the `default` directory:

```bash
# This is where the actual monit program will be installed
monit_executable: '/usr/bin/monit'

# This is used for how often the apt-based tasks will also
# update the cache from the source repo's online.
cache_valid_time_var: 86400

# This is monit's git repo address.
monit_git_repo_http: https://tildeslash@bitbucket.org/tildeslash/monit.git

# This is where the git repo will be cloned to on your destination computer
# This role will actually use the repo to compare version numbers for future
# easy updates.
monit_git_repo_dest: "{{ ansible_env.HOME }}/git/monit"

monit_configure_options: "--enable-optimized"
```

## Example Playbook

    - hosts: servers

      roles:
         - jpartain89.install_monit_from_source

## License

GPLv3

## Author Information

Justin Partain and JPCDI, github.com/jpartain89
