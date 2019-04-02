# Auto-molecule

**Automated testing Ansible roles with Docker and Molecule**

---

## Requirements

1. Install ***Molecule***
2. Install ***Gilt*** - only if you would like to use git overlays or example role...
3. Install ***Docker***
4. Install ***Ansible***
5. Clone this repository and go in to this cloned folder

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

You know, it takes some effort and time to prepare it and We are going to add more features for extend automation with  Molecule.
We will appreciate all donates which we will receive it.

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/cleveritcz)

---

## Usage of donations

 - Extend auto-molecule features
 - Prepare new tools with clever behaviour 
