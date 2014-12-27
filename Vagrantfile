# -*- mode: ruby -*-
# vi: set ft=ruby :

# docs memo     at https://docs.vagrantup.com
# some boxes    at https://atlas.hashicorp.com/search

# variables
# =========
VAGRANTFILE_API_VERSION = "2"

hostname = "ushuaia"
ip_address = "192.168.10.4"
memory = "512"

# specify any relative (../data) or absolute local (/Users/my_username/Sites) path
shared_folder = "/"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    # base box
    # ===============
    config.vm.box = "ubuntu/trusty64"
    config.vm.box_check_update = false

    # port forwarding
    # ===============
    # config.vm.network "forwarded_port", guest: 80, host: 8080

    # private network
    # ===============
    config.vm.network "private_network", ip: ip_address
    config.vm.hostname = hostname

    # public network / like another physical device on the network
    # ==============
    # config.vm.network "public_network"

    # shared forlders "host path", "guest path"
    # ===============
    config.vm.synced_folder shared_folder, "/vagrant"

    # virtualbox conf
    # ===============
    config.vm.provider "virtualbox" do |vb|
        vb.memory = memory
        vb.name = hostname
    end

    # shell prov.
    # ===============
    config.vm.provision :shell, path: "bootstrap.sh"

    # chef_solo prov. (for older versions of vagrant)
    # ===============

    config.librarian_chef.cheffile_dir = "/"

    config.vm.provision :chef_solo do |chef|
        chef.cookbooks_path = "cookbooks"
        chef.add_recipe "git"
    end

end
