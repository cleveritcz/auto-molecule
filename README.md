# Auto-molecule

**Automate tests of Ansible roles with Docker and Molecule**
  - Put your Ansible development to next level

## Release log:

v1.0.4
- added ubuntu 16.04, 18.04 support

v1.0.3
- minor fixes

v1.0.2
- added group_vars for put variables out of the roles
- added possibility to choose what kind of distro will be run for tests  in ***group_vars*** (Debian 8, Debian 9, CentOS 7)
- replaced Gilt with Ansible git module for better manage of git repositories (git.yml)

v1.01
- added auto integration tests (Debian 8, Debian 9, CentOS 7)

v1.00
- auto find all Ansible roles for tests if roles are in folder roles
- auto find and auto fix trailing spaces in yml files for tests
- split molecule and developer code (clean environment for development)
- auto deploy multiple Ansible roles in one container

---

Empty folder ****roles**** is not commited to this repository. 

It will be pulled from github with nginx and tomcat example roles by Ansible when you run: 

```molecule dependency```

---

## Requirements

1. Install ***Molecule***
3. Install ***Docker***
4. Install ***Ansible***
5. Clone this repository and go in to this cloned folder

- libselinux-python (CentOS/RedHat)
---

## Example

We prepared example roles for test functionality of automated testing ansible roles.

Just make these six steps and you will find all features which I added to molecule:

1. Choose from group_vars/all/main.yml distributions for testing
2. Replace git repositories for yours or just leave it as it is for example in git.yml
3. Run **molecule dependency** - it will prepare the environment for test
   - must be run every time when you will change distributions to run
4. Run **molecule test**
   - Validate syntax, lint, fix trailing spaces and make tests
   - It will destroy instance without destroy roles in folder ***roles***
   or/and
5. Run **molecule converge** (Default distro: CentOS 7)
   - start test Ansible roles in docker containers   
6. Run **molecule destroy**
   - Destroy Docker containers and remove all roles from created folder ***roles*** by git.yml

---

## Description

This repository just filling out the spaces of Molecule.

---

## Donation

You know, it takes some effort and time to prepare it and we are going to add more features for extend automation with  Molecule.
We will appreciate all donates which we will receive it.

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/cleveritcz)

---

## Usage of donations

 - Extend auto-molecule features
 - Enjoy new tools with clever behaviour 
