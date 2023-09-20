# BSIO IaC Role - Provision Workstation

## Overview

This Ansible role provisions a workstation, setting up features and tools essential for a developer environment, including Hyper-V.


##### **Note**:

This repository is a subset of the larger BlueServer.io Infrastructure as Code project. For a comprehensive understanding and to get started with the overarching project, please refer to the [main project README](https://github.com/blueserverio/bsio.iac.provision_environment/blob/main/README.md).

## Role Variables

```yaml
---
wait_for_timeout: 900
```

## Dependencies

- [bsio.iac.roles.hyper_v](https://github.com/blueserverio/bsio.iac.roles.hyper_v)

## Example Playbook

```yaml
--- 
- name: Provision Workstation
  hosts: workstation
  gather_facts: no
  tasks:
    - name: Install Hyper-V Feature
      include_role: 
        name: bsio.iac.roles.hyper_v
        tasks_from: install-hyper-v
```

## Contributing
Your contributions are always welcome! If you're looking to contribute to our project, please first read our [CONTRIBUTING guidelines](https://github.com/blueserverio/bsio.iac.provision_environment/blob/main/CONTRIBUTING.md). We look forward to working together to improve and expand the project.


## License
This project is licensed under the [MIT License](LICENSE).