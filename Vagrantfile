Vagrant.configure("2") do |config|
    config.vm.box = "debian/bullseye64"
    config.vm.define "tierra" do |tierra|
      tierra.vm.network "private_network", ip: "192.168.57.103"
      tierra.vm.hostname = "tierra.sistema.test"
      tierra.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y bind9
      SHELL
    end
  
    config.vm.define "venus" do |venus|
      venus.vm.network "private_network", ip: "192.168.57.102"
      venus.vm.hostname = "venus.sistema.test"
      venus.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y bind9
      SHELL
    end
  end
  