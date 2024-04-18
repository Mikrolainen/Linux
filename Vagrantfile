Vagrant.configure("2") do |config|

config.vm.define "debian" do |debian|
  debian.vm.box = "generic/debian12"
  debian.vm.network "public_network"
  debian.vm.network "private_network", ip: "192.168.50.51", virtualbox__intnet: "ansible_lab"
  debian.vm.hostname = "ansible"
  debian.vm.synced_folder "./ansible_data", "/vagrant_data"
  debian.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
	vb.name = "ANSIBLE-mkohava"
    end
  debian.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y git ansible fish tmux mc
  SHELL
  end
config.vm.define "debian2" do |debian2|
  debian2.vm.box = "generic/debian12"
  debian2.vm.network "public_network"
  debian2.vm.network "private_network", ip: "192.168.50.52", virtualbox__intnet: "ansible_lab"
  debian2.vm.hostname = "debian2"
  debian2.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
	vb.name = "DEBIAN2-mkohava"
    end
  debian2.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y git fish tmux mc
  SHELL
  end
config.vm.define "ubuntu" do |ubuntu|
  ubuntu.vm.box = "generic/ubuntu2304"
  ubuntu.vm.network "public_network"
  ubuntu.vm.network "private_network", ip: "192.168.50.53", virtualbox__intnet: "ansible_lab"
  ubuntu.vm.hostname = "ubuntu"
  ubuntu.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
	vb.name = "UBUNTU-mkohava"
    end
  ubuntu.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y git fish tmux mc
  SHELL
  end
config.vm.define "alma" do |alma|
  alma.vm.box = "generic/alma9"
  alma.vm.network "public_network"
  alma.vm.network "private_network", ip: "192.168.50.54", virtualbox__intnet: "ansible_lab"
  alma.vm.hostname = "alma"
  alma.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
	vb.name = "ALMA-mkohava"
    end
  alma.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y git fish tmux mc
  SHELL
  end
end