# Ansible Networking Role

Ansible role to configure the dns resolution to use a specific dns server.

## Requirements

No requirements.

## Dependencies

No dependencies.

## Role Variables

This role contains only two variables:

* `networking_domain_name_server` - The IP Address of the domain name server.
* `networking_interface` - Redhat family network interface override, default `eth0`.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```bash
- hosts: all
  roles:
      - role: neel.networking
        networking_domain_name_server: 192.168.1.1
```

See the molecule tests for more.

## License

Licensed under the MIT License. See the LICENSE file for details.

## Contributing

Feedback, bug-reports, requests, is welcomed and can be done via [github issues](https://github.com/New-Edge-Engineering/ansible-networking/issues).

### Developement Setup

```bash
python3 -m venv .ve
source .ve/bin/activate
pip install molecule molecule-vagrant ansible-lint
molecule test --all
```
