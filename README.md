ushuaia-vagrant
===============

One of my personal virtual machine development environments. (Tested under OS X 10.10 and Debian 7.6 with vagrant v1.7.1)

With vagrant-librarian-chef we don't need to add cookbooks as a git submodule.

## Includes

- Ubuntu 14.04
- git
- Chef (chef_solo used)
- Nginx


### Todo

- nginx-fastcgi
- php-fpm
- php for command line
- mysql
- php extensions
- composer
- node/npm
- bower and grunt
- laravel installer?

## Requirements

* vagrant [(download page)](https://vagrantup.com)
* vagrant-librarian-chef [(a vagrant pluin)](https://github.com/jimmycuadra/vagrant-librarian-chef)

### Optional

- vagrant-omnibus pluin (ability to control the chef version)

By default vagrant uses :latest, but sometimes we need to downgrade to run some recipes.

memo: "config.omnibus.chef_version = :latest"

## Installation

* Clone this git repo, "cd" to it and run/install:

``` bash
vagrant plugin install vagrant-librarian-chef
```

* Remember to set a shared folder in your host machine. (by default is set to the same as Vagrantfile path)

* Run "vagrant up"
    - vagrant-librarian-chef, will read the Cheffile and download all the cookbooks.
