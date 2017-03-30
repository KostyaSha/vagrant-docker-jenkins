# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "fedora/24-cloud-base"

  config.vm.synced_folder ".", "/vagrant", owner: "vagrant", group: "vagrant"
#  config.vm.provision "file", source: "docker.sysconfig", destination: "/etc/sysconfig/docker"
  config.vm.provision "shell", path: "provision.sh"
  config.vm.box_check_update = false

   config.vm.network "private_network", ip: "192.168.33.10"

   config.vm.provider "virtualbox" do |vb|
#     vb.gui = true
     vb.memory = "2024"
   end
end
