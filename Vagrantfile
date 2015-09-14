# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 1
  end

  config.vm.box = "trusty64"

  config.vm.network "private_network", ip: "192.168.150.150"

  config.vm.synced_folder "todos", "/app"

  config.vm.provision "docker"

  config.vm.provision "shell",
    :path => "provision.sh"

  # config.vm.provision "shell",
  #   :path => "config/startup.sh",
  #   run: "always"

end
