ushuaia-vagrant
===============

One of my personal virtual machine development environments. (Tested under OS X 10.10 and Debian 7.6 with vagrant v1.7.1)

With vagrant-librarian-chef we don't need to add cookbooks as a git submodule.

## Includes

- Ubuntu 14.04
- Chef (chef_solo used)
- Nginx
- Node (With Bower and Grunt)


## Requirements

* vagrant [(download page)](https://vagrantup.com)
* vagrant-librarian-chef [(a vagrant pluin)](https://github.com/jimmycuadra/vagrant-librarian-chef)

* Note: older vagrant versions may need vagrant-omnibus plugin, to install latest chef version on the guest machine before provisioning. (config.omnibus.chef_version = :latest)

## Installation

* Clone this git repo, "cd" to it and run/install:

``` bash
vagrant plugin install vagrant-librarian-chef
```

* Remember to set a shared folder in your host machine. (by default is set to the same as Vagrantfile path)

* Run "vagrant up"
    - vagrant-librarian-chef, will read the Cheffile and download all the cookbooks.
