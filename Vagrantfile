# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
 
    #Virtual Machine settings
  
    config.vm.box = "centos/7"
    config.vm.hostname = "cent7"
  
    #Provider settings
  
    config.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.name = "tomcat-utrains"
      vb.cpus = 2
    end
  
    #Network Settings
    
     #config.vm.network "forwarded_port", guest: 80, host: 8080
    # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
    config.vm.network "private_network", ip: "192.168.33.102"
    # config.vm.network "public_network"
  
    #Folder share
     #config.vm.synced_folder ".", "/var/www/html" 
    
    #Provision Settings
    # config.vm.provision "shell", inline: <<-SHELL
    #   apt-get update
    #   apt-get install -y apache2
    #   useradd marc
    # SHELL
    config.vm.provision "shell" , path: "tomcat.sh"
  end