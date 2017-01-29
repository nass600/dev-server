# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "BULLIT"

#   config.vm.network "forwarded_port", guest: 80, host: 8080      #Web
  config.vm.network "forwarded_port", guest: 3306, host: 3306    #MySQL

  config.vm.network "private_network", ip: "192.168.2.200"

  config.ssh.forward_agent = true

  config.vm.synced_folder "../..", "/home/vagrant/Workspace", type: "nfs", :mount_options => ['actimeo=2', 'rw', 'vers=3', 'tcp', 'fsc']

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.name = "dev_server"
  end

  config.vm.provision :ansible do |ansible|
      ansible.playbook = "dev.yml"
  end
end
