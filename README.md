# Ansible Role: Pacemaker

An Ansible Role that installs corosync and pacemaker on Debian/Ubuntu.

## Minimum Ansible Version

2.5

## Requirements

This role requires the [ansible-pacemaker module](https://github.com/egroeper/ansible-pacemaker), which is bundled with the role.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    pm_group: 'nodes'

Group on which pacemaker should be deployed (currently needed for authkey deployment).

    pm_properties: []

Pacemaker properties, that should be configured.


## Dependencies

None.

## Example Playbook

    - hosts: loadbalancer
      roles:
        - { role: ansible-role-pacemaker, pm_groups: "loadbalancer", pm_properties: ["no-quorum-policy=freeze", "stonith-enabled=false"] }

## License

MIT / BSD

## Author Information

This role was created in 2016 by Enno Gröper.
