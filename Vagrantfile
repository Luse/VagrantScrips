# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "precise32"
  config.vm.hostname = "StandAlone"
  config.vm.provision :shell, :path => "vscripts/depend.sh"
  config.vm.provision :shell, :path => "vscripts/apache2.sh"
  config.vm.provision :shell, :path => "vscripts/ruby.sh"
  config.vm.provision :shell, :path => "vscripts/passenger.sh"
  config.vm.provision :shell, :path => "vscripts/passenger-depends.sh"
  config.vm.provision :shell, :path => "vscripts/git.sh"
  config.vm.provision :shell, :path => "vscripts/mongo.sh"
  config.vm.network :forwarded_port, host: 4567, guest: 80
end
