#!/usr/bin/env ruby

Vagrant::Config.run do |config|

  config.vm.box_url = "http://overnothing.com/files/Fedora16.box"
  config.vm.box = "Fedora16"
  
  config.vm.define :'standup-d0' do |db_config|
    config.vm.provision :shell, :inline => "cd /vagrant && ./actions/activate"
    config.vm.customize ["modifyvm", :id, "--memory", 1024, "--cpus", 2]
  end

end

