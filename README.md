# vagrant-lab
This repository is to be used as a guide for helping you install a few tools to aid in learning a variety of Linux/IT skills. I will be using a machine configured like this as the basis for the labs I create for learning material.

# Setting up the environment
In order to run any lab, you will need at a bare minimum the following two pieces of software:
- [Virtualbox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)

In addition, it is recommended that you install a `git` client for your OS.
- [Windows](https://git-scm.com/download/win)
- Linux: install using your package manager
  - ubuntu/debian: `sudo apt-get install git`
  - rhel/centos/fedora: `sudo yum install git`
- OSX: run `xcode-select --install` from the terminal

# Testing the environment
After all of the above software has been installed, download a copy of this repository, extract it, and navigate to the folder in the terminal of your choice:
- Windows: `cmd.exe`, `powershell.exe`, `babun`
- Linux: `gnome-terminal`, `urxvt`, `xterm` etc
- OSX: `Terminal.app`, [iTerm2](https://github.com/gnachman/iTerm2)

From the folder, run the command: `vagrant up`. Vagrant will download the `ubuntu/xenial64` and start a virtual machine in the background.

Once the VM has been started and you return to your shell's prompt, try logging into the VM with `vagrant ssh`

## example:
```
$ vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'ubuntu/xenial64'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'ubuntu/xenial64' is up to date...
==> default: Setting the name of the VM: vagrant-lab_default_1510623605345_58237
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
...
    default: Guest Additions Version: 5.0.40
    default: VirtualBox Version: 5.2
==> default: Mounting shared folders...
    default: /vagrant => /home/dyindude/projects/vagrant-lab
$ vagrant ssh
Welcome to Ubuntu 16.04.3 LTS (GNU/Linux 4.4.0-98-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.


ubuntu@ubuntu-xenial:~$ 
```

# Contact
If you run into issues with the setup, feel free to reach out to me:

- https://twitch.tv/dyindude
- https://twitter.com/dyindude
