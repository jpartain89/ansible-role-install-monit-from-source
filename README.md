jpartain89.ansible_monit_from_source [![Build Status](https://travis-ci.org/jpartain89/ansible_monit_from_source.svg?branch=master)](https://travis-ci.org/jpartain89/ansible_monit_from_source)
=========

Installation of monit from their Git Repo

Role Variables
--------------

```
monit_git_repo_http: https://tildeslash@bitbucket.org/tildeslash/monit.git
monit_git_repo_dest: "{{ ansible_user_dir }}/git/monit"
monit_configure_options: --enable-optimized
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - jpartain89.ansible_monit_from_source

License
-------

GPLv3

Author Information
------------------

Justin Partain and JPCDI, github.com/jpartain89
