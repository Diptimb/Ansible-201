# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant VM cofigurations
   config.vm.box = "ubuntu/trusty64"
   config.ssh.insert_key = false
   config.vm.synced_folder ".", "/vagrant", disabled: true
   config.vm.provider :virtualbox do |v|
     v.memory = 256
     v.linked_clone = true
   end
   # Application server 1
   config.vm.define "app1" do |app|
     app.vm.hostname = "ansible-test-server1"
     app.vm.network :private_network, ip: "192.168.60.4"
   end
end
