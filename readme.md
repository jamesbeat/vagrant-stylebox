#Introduction

This covers the Intallation and setup of a Drupal Multisite instance on a Vagrant Box hosted on a remote Machine , controlled vie Drush from a remote Machine.

Terms:

Local Machine: The Machine you are currently sitting in front of

Remote Host Machine: The Server hosting your Vagrant Box virtualization Environment

Remote Guest Machine: The virtual Server hosted on the Remote Host Machine


#Installation

Download Vagrant from
[www.vagrantup.com/downloads](http://www.vagrantup.com/downloads)

Download Virtualbox from
[www.virtualbox.org](https://www.virtualbox.org/)


```shell
$ mkdir vagrant_project
$ cd vagrant_project
$ vagrant init
```

#Setup

```shell
$ vagrant plugin install vagrant-vbguest
```

#Launch

```shell
$ sudo vagrant up
```

#Interact

## Login on Host Machine

```shell
$ vagrant ssh
```

## Login from Remote Machine

### Getting Keys

Copy private key from Host Machine at puphpet/files/dot/ssh/id_rsa to your remote machine, for example in directory /Users/Basti/.ssh/stylebox/id_rsa

```shell
$ ssh vagrant@10.0.1.28 -o PasswordAuthentication=no -i /Users/Basti/.ssh/stylebox/id_rsa -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -p 2223
```


##Databases

Run Adminer via /adminer to administer the MySQL Databases


#Installing Drupal on Remote Guest Machine

