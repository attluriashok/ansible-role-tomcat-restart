# **Ansible Role: Tomcat Restart**

This role is used to restart a tomcat service.

## Requirements

This role only requires Ansible version 1.8+.

## Role Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
---

# Tomcat info
tomcat_path: /opt/tomcat # (required)
tomcat_port: 8080        # (required)

```

## Dependencies

None

## Example Playbook

```yaml
---

- hosts: all

  vars:
    tomcat_path: /opt/tomcat
    tomcat_port: 8080

  roles:
    - { role: ansible-role-deploy-java, tags: [ 'stop', 'start' ] }

```

## License

MIT / BSD

## Author Information

Thiago Gomes


