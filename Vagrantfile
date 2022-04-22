Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.56.10"
  config.vm.provision "file", source: "./default_folder/default1", destination: "/home/vagrant/etc/nginx/sites-available/"
  config.vm.synced_folder ".", "/home/vagrant/app"
  # config.vm.synced_folder "default1", "/home/vagrant/etc/nginx/sites-available/"
  config.vm.provision "shell", path: "./provision.sh"

end
