# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.box_version = "20180213.2.0"
  config.vm.hostname = "BULLIT"
  config.vm.network "private_network", ip: "192.168.3.200"
  config.ssh.forward_agent = true
  config.vm.synced_folder "../..", "/home/vagrant/Workspace", type: "nfs", :mount_options => ['actimeo=2', 'rw', 'vers=3', 'tcp', 'fsc']
  config.vm.synced_folder "../../../Downloads/Test", "/home/vagrant/Downloads", type: "nfs", :mount_options => ['actimeo=2', 'rw', 'vers=3', 'tcp', 'fsc']

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.name = "dev_server"
  end

  config.vm.provision :ansible do |ansible|
      ansible.playbook = "dev.yml"
  end
end
