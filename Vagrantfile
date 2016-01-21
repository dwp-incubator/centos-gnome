# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
    config.vm.box           = "centos/7"
    config.vm.network       "private_network", ip: "192.168.56.50"

    config.vm.provider :virtualbox do |vb|
        vb.name = "centos-gnome"
        vb.cpus = 2
        vb.memory = "4096"
        vb.gui = true
        vb.customize ["modifyvm", :id, "--vram", "64"]
        vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end

    config.vm.provision :ansible do |ansible|
        ansible.playbook = 'default.playbook'
    end
end
