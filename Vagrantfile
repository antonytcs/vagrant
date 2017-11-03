# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.define :server1 do |server1_centos|
      server1_centos.vm.hostname="anto.server1.local"
      server1_centos.vm.box="centos/7"
      server1_centos.vm.network "private_network", ip: "192.168.1.200"
      #server1_centos.vm.network "private_network", type: "dhcp"
      server1_centos.vm.provision "shell", path: "httpd.sh"
  end
  config.vm.define :server2 do |server2_centos|
       server2_centos.vm.hostname="anto.server2.local"
       server2_centos.vm.box="centos/7"
       server2_centos.vm.network "private_network", ip: "192.168.1.201"
       #server2_centos.vm.network "private_network", type: "dhcp"
       server2_centos.vm.provision "shell", path: "httpd.sh"
end

config.vm.define :server3 do |server3_ubuntu|
      server3_ubuntu.vm.hostname="anto.server3.local"
      server3_ubuntu.vm.box="ubuntu/trusty64"
      server3_ubuntu.vm.network "private_network", ip: "192.168.1.202"
      #server3_ubuntu.vm.network "private_network", type: "dhcp"
      server3_ubuntu.vm.provision "shell", path: "ubuntu.sh"

end

config.vm.define :server4 do |server4_rhel|
      server4_rhel.vm.hostname="anto.server4.local"
      server4_rhel.vm.box="iamseth/rhel-7.3"
      server4_rhel.vm.network "private_network", ip: "192.168.1.203"
      #server4_rhel.vm.network "private_network", type: "dhcp"

end


config.vm.define :server5 do |server5_windows2012|
      server5_windows2012.vm.hostname="anto.server5.local"
      server5_windows2012.vm.box="opentable/win-2012r2-standard-amd64-nocm"
      server5_windows2012.vm.network "private_network", ip: "192.168.1.204"
      #server5_windows2012.vm.network "private_network", type: "dhcp"

end



  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
