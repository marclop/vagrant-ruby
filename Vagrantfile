# -*- mode: ruby -*-
# vi: set ft=ruby :

$memory = 512

Vagrant.configure(2) do |config|

  config.vm.box = "chef/centos-7.0"

  config.vm.synced_folder "./data", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = $memory
  end

  config.vm.provision "shell", inline: <<-SHELL
    sudo yum install ruby -y -q
    sudo hostnamectl set-hostname ruby
   SHELL
end
