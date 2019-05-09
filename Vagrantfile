Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  
  # Configuration for VirtualBox:
  config.vm.provider "virtualbox" do |vb|
  # Display the VirtualBox GUI when booting the machine
  vb.gui = true
  # Customize the amount of memory on the VM:
  vb.memory = "2048"
  end
 
 # Begin Configuring
config.vm.define "lamp" do|lamp|

lamp.vm.hostname = "lamp" # Setting up hostname
lamp.vm.network "private_network", ip: "192.168.205.10" # Setting up machine's IP Address
end

lamp.vm.provision :shell, path: "/scripts/lamp.sh" # Provisioning with script.sh
# End Configuring
end
