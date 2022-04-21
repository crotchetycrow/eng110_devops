Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.56.10"
  # config.vm.provision "file", source: "~/.gitconfig", destination: ".gitconfig"
  config.vm.synced_folder ".", "/home/vagrant/app"
  # config.vm.synced_folder "./app", "/app"

end
