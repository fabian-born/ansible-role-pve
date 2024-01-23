# ansible-role-pve_vm

### Example to deploy/clone a vm

```yaml
---
- hosts: localhost
  gather_facts: false

  vars_prompt:
    - name: env_name
      prompt: What environment do we deploy?
      private: false

  vars_files:
    - vars/secrets.yaml

  roles:
    - env_vars
    - pve_vm
```


vm config file:
```yaml
---
- hosts: localhost
  gather_facts: false

  vars_prompt:
    - name: env_name
      prompt: What environment do we deploy?
      private: false

  vars_files:
    - vars/secrets.yaml

  roles:
    - env_vars
    - pve_vm
```


default config file:
```yaml
---
pve_node: pve-node
pve_api_node: ip-addr/hostname
pve_os_template: "ubuntu-2204-template"
guest_network: ""
# description: "first test"
# vm_state: "present"
```
