# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "sbeliakou/centos-6.7-x86_64"
  #config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "private_network", ip: "192.168.56.24"

  config.vm.hostname = "zabbix1"
  
  config.vm.provider "virtualbox" do |vb|
    vb.name = "zabbix1"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = 'provision.yml'
    ansible.verbose = 'vv'
  end
end
