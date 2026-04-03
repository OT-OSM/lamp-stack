
## Ansible Role: LAMP Stack 
[LAMP stack Image](https://github.com/OT-OSM/lamp-stack/blob/LAMP/static/LAMP.png)

### Version History

|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|**MAY '29'** | v.1.0 | Initial Draft | Pritam Kondapratiwar |



## Table of Content
- [Introduction](#introduction)
- [Salient Features](#salient-features)
- [Supported OS](#supported-os)
- [Directory Structure](#directory-structure)
- [Role Variables](#role-variables)
- [Inventory](#inventory)
- [References](#references)


### Introduction

**LAMP** is a group of open-source software used together to run websites and web applications. It's called a **stack** because each layer works on top of the other.

**LAMP** stands for:

- **L – Linux**: The operating system (like Windows, but open-source).
- **A – Apache**: The web server software that shows your website in browsers.
- **M – MySQL**: The database system that stores your website’s data (like users, posts, etc.).
- **P – PHP**: The programming language used to create the website logic.


### Salient Features

- **Open Source**: All components of LAMP are free and open-source, reducing software costs.
- **Cross-Platform Support**: While originally designed for Linux, LAMP can be adapted to other platforms like Windows (WAMP) and macOS (MAMP).
- **Flexible and Customizable**: Developers can modify components to suit their project needs.
- **Community Support**: Large and active community support for all LAMP components.

### Supported OS
------------
  * Ubuntu 20.10 and above
  * Debian 11 and above
  * RHEL 8.2 and above

### Directory Structure

#### For LAMP stack
```
├── defaults
│   └── main.yml
├── handlers
│   └── main.yml
├── meta
│   └── main.yml
├── README.md
├── tasks
│   ├── debian.yml
│   ├── main.yml
│   └── redhat.yml
```

### Role Variables

|**Variables**| **Default Values**| 
|----------|---------|
| **server url** | http://127.0.0.1 | 

## Inventory

An inventory should look like this:-
#### For LAMP stack
```ini
[LAMP stack host]                 
13.xxx.xxx.xx    ansible_user=ubuntu   

```

Example Playbook
----------------

* Here is an example playbook:-
#### For LAMP stack
```sh
---
- hosts: LAMP stack host
  become: yes
  roles:
    - lampstack

```

## References
----------
- **[software](https://www.digitalocean.com/community/tutorials/how-to-install-lamp-stack-on-ubuntu)**
