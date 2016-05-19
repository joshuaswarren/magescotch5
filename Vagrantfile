# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    config.vm.box = "creatuity/MageScotchBox5"
    config.vm.network "private_network", ip: "192.168.33.10"
    config.vm.provision :shell, path: "bootstrap.sh"
    config.vm.hostname = "magescotch5"
    config.vm.synced_folder "./", "/var/www", type:"nfs", mount_options:["nolock,vers=3,udp,noatime,actimeo=1"] 
    config.vm.provider "virtualbox" do |v|
  	v.memory = 4096
  	v.cpus = 4
    end
end
