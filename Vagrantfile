# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-14.04"

  config.vm.network "forwarded_port", host: 8000, guest: 80

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "CoGe"
    # Display the VirtualBox GUI when booting the machine
    vb.gui = false
    vb.cpus = 2
    vb.memory = 1024
  end
 
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "coge_playbook.yml"
  end

end
