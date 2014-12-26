ushuaia-vagrant
===============

One of my personal virtual machine development environments. (Tested under OS X 10.10 and Debian 7.6 with vagrant v1.7.1)

With vagrant-librarian-chef we don't need to add cookbooks as a git submodule.

## Requirements

* vagrant [(download page)](https://vagrantup.com)
* vagrant-librarian-chef [(a vagrant pluin)](https://github.com/jimmycuadra/vagrant-librarian-chef)

* Note: older vagrant versions may need vagrant-omnibus plugin, to install latest chef version on the guest machine before provisioning. (config.omnibus.chef_version = :latest)

## Installation

* Clone this git repo and "cd" to the vagrant folder and run/install:

``` bash
vagrant plugin install vagrant-librarian-chef
```
* Run "vagrant up"
    - vagrant-librarian-chef, will read the Cheffile and download all the cookbooks.
