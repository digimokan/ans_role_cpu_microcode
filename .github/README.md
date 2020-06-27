# ans-role-cpu-microcode

Ansible role to configure CPU microcode updates to load at boot.

[![Release](https://img.shields.io/github/release/digimokan/ans-role-cpu-microcode.svg?label=release)](https://github.com/digimokan/ans-role-cpu-microcode/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Load Role Via Ansible Galaxy](#load-role-via-ansible-galaxy)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install correct CPU microcode package(s) for _Intel_ or _AMD_ CPU.
* Configure bootloader to load CPU microcode.

## Supported Operating Systems

* Arch Linux (with _GRUB_ bootloader)

## Quick Start

### Load Role Via Ansible Galaxy

1. Create `requirements.yml` in ansible project root, and add this content:

   ```
   # requirements.yml
   - src: https://github.com/digimokan/ans-role-cpu-microcode
     version: master
     name: config-cpu-microcode
   ```

2. From the project root directory, install the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles
   ```

3. Include the role like any local role, from the project playbook:

   ```
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Configure CPU microcode to load at boot"
         include_role:
           name: config-cpu-microcode
   ```

## Role Options

See the role `defaults` file for full listing:

  * [defaults/main.yml](../defaults/main.yml)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans-role-cpu-microcode/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

