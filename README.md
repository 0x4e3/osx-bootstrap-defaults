# osx-bootstrap-defaults

The role to set "defaults" on OSX.

[![Build Status](https://travis-ci.org/0x4e3/osx-bootstrap-defaults.svg?branch=master)](https://travis-ci.org/0x4e3/osx-bootstrap-defaults)
[![GitHub license](https://img.shields.io/github/license/0x4e3/osx-bootstrap-defaults.svg)](https://github.com/0x4e3/osx-bootstrap-defaults/blob/master/LICENSE)

## Requirements

No.

## Role Variables

* ```osx_defaults``` -- the list of defaults.

## Dependencies

No.

## Example Playbook

```playbook.yml```:
```yml
---
- host: localhost
  vars_files:
    - vars/defaults.yml
  roles:
    - 0x4e3.osx-bootstrap-defaults
```

```vars/defaults.yml```
```yml
---
osx_defaults:
  - domain: 'NSGlobalDomain'
    key: 'NSTableViewDefaultSizeMode'
    type: int
    value: 1
  - domain: 'NSGlobalDomain'
    key: 'NSNavPanelExpandedStateForSaveMode'
    type: bool
    value: true
  - domain: 'NSGlobalDomain'
```
