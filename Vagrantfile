# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "BULLIT"

  config.vm.network "forwarded_port", guest: 80, host: 8080      #Web
  config.vm.network "forwarded_port", guest: 3000, host: 3000    #BrowserSync
  config.vm.network "forwarded_port", guest: 3306, host: 3306    #MySQL
  config.vm.network "forwarded_port", guest: 9876, host: 9876    #Karma
  config.vm.network "forwarded_port", guest: 27017, host: 27017  #MongoDB

  config.vm.network "private_network", ip: "192.168.2.200"

  config.ssh.forward_agent = true

  config.vm.synced_folder "../..", "/home/vagrant/Workspace", type: "nfs", :mount_options => ['actimeo=2', 'rw', 'vers=3', 'tcp', 'fsc']

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.name = "nass600_server"
  end

  config.vm.provision :ansible do |ansible|
      ansible.playbook = "provision/vagrant.yml"
  end
end
