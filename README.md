# Auto-molecule

**Automate tests Ansible roles with Docker and Molecule**


## Release log:
---

v1.01
- added auto integration tests (Debian 8, Debian 9, CentOS 7)

v1.00
- auto find all Ansible roles for tests if roles are in folder roles
- auto find and auto fix trailing spaces in yml files for tests
- split molecule and developer code (clean environment for development)
- auto deploy multiple Ansible roles in one container

---

Empty folder ****roles**** is not commited to this repository. 

It will be created with nginx example role which it will start clone to your folder when you run: 

```molecule dependency```

---

## Requirements

1. Install ***Molecule***
2. Install ***Gilt*** - only if you would like to use git overlays or example role...
3. Install ***Docker***
4. Install ***Ansible***
5. Clone this repository and go in to this cloned folder

- libselinux-python (CentOS/RedHat)
---

## Example

We prepared example role for test functionality of automated testing ansible roles.

Just make these three steps and you will find all features which I added to molecule:


1. Run **molecule converge** (Default distro: CentOS 7) or 
   **MOLECULE_DISTRO=debian9 molecule converge** - run Ansible role on Debian 9
   - Clone git repository to folder roles/ and find all Ansible roles in folder ***roles***, run them in Docker containers
2. Run **molecule test**
   - Validate syntax, lint, fix trailing spaces and make tests  
3. Run **molecule destroy**
   - Destroy Docker container and remove all roles from created folder ***roles***

---

## Description

This repository just filling out the space between Molecule, Ansible, Gilt and Docker.

---

## Donation

You know, it takes some effort and time to prepare it and we are going to add more features for extend automation with  Molecule.
We will appreciate all donates which we will receive it.

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/cleveritcz)

---

## Usage of donations

 - Extend auto-molecule features
 - Enjoy new tools with clever behaviour 
