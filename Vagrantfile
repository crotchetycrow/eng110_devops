Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/xenial64"
  #Create a private network with provided IP address
  config.vm.network "private_network", ip: "192.168.56.10"  

  config.vm.provision "shell", path: "provisioning.sh"

  # config.trigger.after [:up, :provision] do |trigger|
  #   trigger.info = "Running ./provisioning.sh locally..."
  #   trigger.run = {path: "./provisioning.sh"}
  # end
end
