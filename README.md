# Ubuntu Server Config

These are my own personal notes for configuring a Ubuntu server that is being developed virtually using [VirtualBox](https://www.virtualbox.org/) and accessed with [Vagrant](https://www.vagrantup.com/). This document is likely to change heavily, as I continue to learn this process I will continue to organize sections more effectively.

### Initialize Vagrant

To create a new virtual machine using Vagrant, from the working directory `$ vagrant init ubuntu/trusty64`. Trusty64 represents Ubuntu Server 14.04.3 LTS. Run `$ vagrant up`, the first time this is run the virtual machine will be downloaded. `$ vagrant ssh`, cool we're in Ubuntu.

### Update Ubuntu

* `$ sudo apt-get update` - Download and update all of our packages.
* `$ sudo apt-get upgrade` - Install all of those new packages.

Combine them with `&&` to start getting fancy.

### Vagrant and Ubuntu User Security

Vagrant does us a favor here and disables `root` user SSH while creating a new user named `vagrant` with `sudo` powers. Let's break that down.

If that wasn't the case add a new user and grant `sudo` powers:

* `$ sudo adduser username`, provide a password and any optional additional information.
* `$ sudo nano /etc/sudoers.d/username` and add `student ALL=(ALL) NOPASSWD:ALL`, write out and exit.
* If you'd like to connect to that new using through Vagrant `$ ssh username@127.0.0.1 -p 2222`

If you need to disable `root` SSH manually follow this [How-To-Geek article](http://www.howtogeek.com/howto/linux/security-tip-disable-root-ssh-login-on-linux/) and check the comments for additional security ideas.

### Key Based Authentication
