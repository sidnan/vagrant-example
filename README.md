vagrant-example
===============

Example Vagrant script to access virtual machine


This repo contains example script to access virtual machine using
* the vagrant box created with Packer
* vagrant software and virtual box product


# This is helpful to know

* Vagrant basics to access virtual machine


# Used

* [Packer v0.5.2](http://www.packer.io/docs)
* [Vagrant v1.3.5](https://docs.vagrantup.com/v2/getting-started/)


# Technology choice

Can set up a file - describe the type of machine, the box, and the way to access the machine. And access the machine using simple command.

This helps to provide fast development, maintainability, and portability.




# Steps to vagrant up box

1. Get into the directory which holds the "Vagrantfile"
2. vagrant box remove <box name> => vagrant box remove ubuntu1404-provisionerless
3. vagrant box add <box name> <box path> => vagrant box add ubuntu1404-provisionerless virtualbox/ubuntu1404-provisionerless.box
4. vagrant init (init based on the vagrantfile and setup a directory vagrant which holds entities like shares- /vagrant/init/shares, /vagrant/init/init.sh, etc. "/vagrant" is the local home directory.)
5. vagrant up (brings up the machine)
6. vagrant ssh (access the machine)


# Other useful commands

* vagrant suspend (to suspend) AND vagrant resume (to resume)
* vagrant destroy (to destroy the machine. which needs bring up to access again)
* vagrant -h => for vagrant help