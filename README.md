# Ansible Role: Pacemaker

An Ansible Role that installs corosync and pacemaker on Debian/Ubuntu.

## Minimum Ansible Version

1.7

## Requirements

This role requires the [pacemaker ansible module](https://github.com/egroeper/ansible-pacemaker).

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
        - '{ role: "https://github.com/hu-berlin-cms/ansible-role-pacemaker.git", pm_groups: "loadbalancer", pm_properties: ["no-quorum-policy=freeze", "stonith-enabled=false"] }'

## License

MIT / BSD

## Author Information

This role was created in 2016 by Enno Gröper.
