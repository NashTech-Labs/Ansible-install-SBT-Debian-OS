Using Ansible to  install SBT on a debian system with all prerequisite language installation
=========
![CI](https://github.com/knoldus/Ansible-Role-Docker-Compose-Debian/blob/main/CI-passing.svg)

This template contains both a playbook and an Ansible Role that installs SBT with Java and Scala on Linux with Debian distros.

Requirements
------------
* Python  : ``` sudo apt install python3 ```
* Ansible : you refer to [Ansible Installation](./InstallAnsible.md) for steps

* Ansible Prerequisites:

  * **One Ansible Control Node:** The Ansible control node is the machine we’ll use to connect to and control the Ansible hosts over SSH. Your Ansible control node can either be your local machine or a server dedicated to running Ansible, though this guide assumes your control node is an Ubuntu 20.04 system. Make sure the control node has:

    * A **non-root user** with sudo privileges. To set this up, you can follow Steps 2 and 3 of our [Initial Server Setup](./SetUpServer.md). However, please note that if you’re using a remote server as your Ansible Control node, you should follow every step of this guide. Doing so will configure a firewall on the server with ufw and enable external access to your non-root user profile, both of which will help keep the remote server secure.

    * An **SSH keypair** associated with this user. To set this up, you can follow Step 1 of [Set Up SSH Keys on Ubuntu](./SetUpSSHkey.md).

  * One or more **Ansible Hosts**: An Ansible host is any machine that your Ansible control node is configured to automate. This guide assumes your Ansible hosts are remote Ubuntu 20.04 servers. Make sure each Ansible host has:

    * The Ansible control node’s SSH public key added to the authorized_keys of a system user. This user can be either root or a regular user with sudo privileges. To set this up, you can follow Step 2 of [Set Up SSH Keys on Ubuntu](./SetUpSSHkey.md).


Role Variables
--------------

Variables used in this are just the version:


Dependencies
------------
None

Example Playbook
------------

```yaml
- hosts: all
  roles:
    - UsingRole
```

Author Information
------------------

Created by [Vaibhav Kumar](https://github.com/vaibhavkumar779)
