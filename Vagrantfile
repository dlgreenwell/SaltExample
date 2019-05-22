#script to create vagrant box pulled from 

Vagrant.configure("2") do |config|
  config.vm.box = "mwrock/Windows2016"
  
   ## I'm guessing this is different for windows
    config.vm.synced_folder "salt/roots/", "/srv/salt/"

    ## Use all the defaults:
    config.vm.provision :salt do |salt|

      salt.masterless = true
      salt.minion_config = "salt/minion"
      salt.run_highstate = true
end
