# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network :private_network, ip: "10.170.0.2"

  config.vm.provider :virtualbox do |vb|
  #   # Don't boot with headless mode
  #   vb.gui = true
  #
  #   # Use VBoxManage to customize the VM. For example to change memory:
      vb.customize ["modifyvm", :id, "--memory", "2048"]
  end

  config.vm.provision :shell, :path => "bootstrap.sh"
  config.vm.hostname = 'sensumaster.vagrant'

  config.vm.provision :puppet do |puppet|
     puppet.hiera_config_path = "hiera.yaml"
     puppet.manifests_path = "manifests"
     puppet.manifest_file  = "puppet.pp"
  end

#  config.vm.network :private_network, :ip => '10.239.0.2'
end
