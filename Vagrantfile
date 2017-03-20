# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_FILE_VERSION = 2

Vagrant.configure(VAGRANT_FILE_VERSION) do |config|

  config.vm.box        = 'ebrc/centos-7-64-puppet'

  config.ssh.username  = 'vagrant'
  config.ssh.password  = 'vagrant'
  config.ssh.insert_key = 'true'

  config.vm.define :genifrdev do |genifrdev_config|
	genifrdev_config.vm.network :private_network, :ip => "192.168.70.10"
  end

  config.vm.provision "puppet" do |puppet|
  	puppet.environment_path = "environments"
  	puppet.environment 	= "development"
 	puppet.module_path      = "puppet/modules"
  end
end
