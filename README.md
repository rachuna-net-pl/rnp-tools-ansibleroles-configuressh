rnp-tools-ansibleroles-configuressh
=========

Configuration SSH roles

![Overwiew](https://gitlab.com/rachuna-net.pl/tools/ansibleroles/rnp-tools-ansibleroles-configuressh/-/raw/master/docs/configurationSSH.png)

Role Variables
--------------

Defaults role values:
```yaml
input_role_os_distribution: Ubuntu

input_role_ssh_configuration:
  PasswordAuthentication: "no"
  Port: 22
  PermitRootLogin: "no"
```

Role vars
```yaml
vars_sshd_config_path: /etc/ssh/sshd_config
```

Example Playbook
----------------

```yaml
    - hosts: servers
      become: yes
      roles:
        - role: rnp-tools-ansible-roles-configuressh
          vars:
            input_role_os_distribution: "{{ ansible_distribution }}"
            input_role_ssh_configuration:
              PasswordAuthentication: "no"
              Port: 22
              PermitRootLogin: "no"
```

License
-------

BSD 3-Clause

Author Information
------------------

### Maciej Rachuna
SysOps/DevOps