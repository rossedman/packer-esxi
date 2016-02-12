# -*- mode: ruby -*-
# vi: set ft=ruby :

nodes = [
  { :hostname => 'esx-01a', :box => 'yourname/esxi'},
  { :hostname => 'esx-02a', :box => 'yourname/esxi'},
  { :hostname => 'esx-03a', :box => 'yourname/esxi'},
]

Vagrant.configure('2') do |config|
  nodes.each do |node|
    config.vm.define node[:hostname] do |node_config|
      node_config.ssh.username = 'root'
      node_config.ssh.shell = 'sh'
      node_config.ssh.insert_key = false
      node_config.vm.synced_folder '.', '/vagrant', disabled: true
      
      node_config.vm.box = node[:box]
      node_config.vm.hostname = node[:hostname]
      node_config.vm.network "public_network"
    end
  end
end