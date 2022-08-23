# Ansible Role : manage_selinux

[![CI](https://github.com/glillico/ansible-role-manage_selinux/workflows/CI/badge.svg)](https://github.com/glillico/ansible-role-manage_selinux/actions?query=workflow%3ACI)

This role manages the state of selinux.

## Requirements

None.

## Role Variables

### defaults/main.yml

|Variable|Description|
|---|:---|
|mse_policy|Defines the name of the SELinux policy to use.||
|mse_state|Defines the SELinux mode.<br>(Options: disabled, enforcing, permissive).|
|mse_kernel_param|If set to `true' it will update the kernel boot parameters when enabling or disabling SELinux.<br>(Options: true, false).|

## Dependencies

None.

## Example Playbook

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - glillico.manage_selinux

## License

MIT

## Author Information

This role was created in 2021 by Graham Lillico.
