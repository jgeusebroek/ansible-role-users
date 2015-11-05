# Ansible role: ca_certs

Manage system user accounts and groups. Tested on RedHat/CentOS or Debian/Ubuntu but should work for most Linux distributions / flavours.

## Requirements

None

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
         - { role: jgeusebroek.users, tags: ["users"] }

## Example Variables

    users_available:
      - username: foo
        uid: 1001
        name: "Foo"
        upload_key: true
        home_dir: "/var/www/foo"
        auth_file: "foo.pub"
      - username: bar
        uid: 1002
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

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Jeroen Geusebroek](http://jeroengeusebroek.nl/).