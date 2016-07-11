# ansible-role-yum-cron

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-yum-cron.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-yum-cron)

RHEL/CentOS - Call yum from cron

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    yum_cron_base_debuglevel: -2
    yum_cron_base_mdpolicy: 'group:main'
    yum_cron_commands_apply_updates: False
    yum_cron_commands_download_updates: True
    yum_cron_commands_random_sleep: 360
    yum_cron_commands_update_cmd: default
    yum_cron_commands_update_messages: True
    yum_cron_email_email_from: root@localhost
    yum_cron_email_email_host: localhost
    yum_cron_email_email_to: root
    yum_cron_emitters_emit_via: stdio
    yum_cron_emitters_ouput_width: 80
    yum_cron_emitters_system_name: None
    yum_cron_groups_group_list: None
    yum_cron_groups_group_package_types: [ 'mandatory', 'default' ]
    yum_cron_hourly_base_debuglevel: -2
    yum_cron_hourly_base_mdpolicy: 'group:main'
    yum_cron_hourly_commands_apply_updates: False
    yum_cron_hourly_commands_download_updates: False
    yum_cron_hourly_commands_random_sleep: 15
    yum_cron_hourly_commands_update_cmd: default
    yum_cron_hourly_commands_update_messages: False
    yum_cron_hourly_email_email_from: root
    yum_cron_hourly_email_email_host: localhost
    yum_cron_hourly_email_email_to: root
    yum_cron_hourly_emitters_emit_via: stdio
    yum_cron_hourly_emitters_ouput_width: 80
    yum_cron_hourly_emitters_system_name: None
    yum_cron_hourly_groups_group_list: None
    yum_cron_hourly_groups_group_package_types: [ 'mandatory', 'default' ]

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.yum-cron
          yum_cron_commands_apply_updates: True
          yum_cron_commands_download_updates: True
          yum_cron_emitters_emit_via: None
          yum_cron_hourly_commands_apply_updates: True
          yum_cron_hourly_commands_download_updates: True
          yum_cron_hourly_emitters_emit_via: None

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
