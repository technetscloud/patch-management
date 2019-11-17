[![Build Status](https://travis-ci.org/technetscloud/patch-management.svg?branch=master)](https://travis-ci.org/technetscloud/patch-management)

## Introduction

#### Dependencies
- The module we are using is only supported from ansible 2.9
- `python-apt` is required ar remote machines.

>> This role currently support only Ubuntu. :cry:


As you already know, patch manageent is very important in Server infrastracture as new vilnerablilities are detected  and needs to be patched daily. 

If you have only one or two servers, patching is not very difficult, what if you have hundred of servers running different applications.

#### Using ansible for Patch Management

Ansible role for patch management. It is not safe to update all packages as which ma c break the application itself due to dependencies. For this we have to decide which all application should not be updated during the regular patch management cycle.

#### How to use
Fillout the defaults/main.yml as per your requirement.

Create a playbook with host group you need to patch

```yaml
---
- hosts: all
  become: yes
  roles:
  	- patch-management
```
