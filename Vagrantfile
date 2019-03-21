Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.100.199"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
  end

  # folders to mount
  config.vm.synced_folder "./", "/var/www/html"

  config.vm.provision "shell" do |s|
      s.path = ".vagrant/provision.sh"
  end

end
