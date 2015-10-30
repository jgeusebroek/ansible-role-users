Users
=========

Manage system user accounts and groups

Requirements
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: jgeusebroek.users }

Example Variables
----------------

    users_available:
      - username: foobar
        uid: 1010
        name: "Foo Bar"
        upload_key: true
        home_dir: "/var/www/bla"
        auth_file: "foobar.pub"
      - username: helloworld
        uid: 1020
        name: "Hello World"
        upload_key: true

    users_deleted:
      - barfoo

    users_groups_available:
      - groupname: admin
        gid: 1050
      - groupname: sysgroup
        gid: 801
        is_system_group: true

    users_groups_deleted:
      - deleteme

License
-------

BSD

Author Information
------------------

Jeroen Geusebroek
me@jeroengeusebroek.nl