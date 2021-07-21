
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "forwarded_port", guest: 8080, host: 8080, host_ip: "10.174.97.150" 
  config.vm.synced_folder ".", "/mnt/host_machine"
  config.vm.provider :virtualbox do |vb|
      vb.name = "jenkinstest"
      vb.memory = "2048"
  end
  config.vm.provision "shell" do |s|
    s.path = "provision.sh"
  end
end
