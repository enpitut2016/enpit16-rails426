Vagrant.configure(2) do |config|
  config.vm.box = "chiemi627/enpit16-rails4.2.6"
  config.vm.box_version = "1.0.1"
  config.ssh.insert_key = false
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.synced_folder "./workspace", "/home/vagrant/workspace"
end

