Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/xenial64"
  #Create a private network with provided IP address
  config.vm.network "private_network", ip: "192.168.56.10"  

  config.vm.provision "shell", path: "provisioning.sh"

  # config.trigger.before :up, :provision do |trigger|
  #   trigger.run = {inline: "provisioning.sh"}
  # end
end
