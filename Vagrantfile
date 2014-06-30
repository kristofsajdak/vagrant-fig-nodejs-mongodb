# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "phusion-open-ubuntu-14.04-amd64"

    config.vm.network "forwarded_port", guest: 8080, host: 8085
    config.vm.network "forwarded_port", guest: 5858, host: 5858
    config.vm.network "forwarded_port", guest: 27017, host: 27017

    config.vm.provision "docker" do |d|
    end

    config.vm.provision "shell", path: "provision_fig.sh"
    config.vm.provision "file", source: "fig.yml", destination: "fig.yml"

end
