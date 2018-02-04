# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 config.vm.define :nodo1 do |nodo1|
    nodo1.vm.box = "debian/stretch64"
    nodo1.vm.hostname = "nodo1"
    nodo1.vm.network :private_network, ip: "10.0.1.1/24",
        virtualbox__intnet: "redinterna"
    nodo1.vm.network :private_network, ip: "10.10.1.1/24"
    nodo1.vm.provision "ansible" do |ansible|
	ansible.inventory_path = "hosts"
	ansible.playbook = "playbooks/node1.yaml"
    end
  end
 config.vm.define :nodo2 do |nodo2|
    nodo2.vm.box = "debian/stretch64"
    nodo2.vm.hostname = "nodo2"
    nodo2.vm.network :private_network, ip: "10.0.1.2/24",
	virtualbox__intnet: "redinterna"
    nodo2.vm.network :private_network, ip: "10.10.1.2/24"
    nodo2.vm.provision "ansible" do |ansible|
	ansible.inventory_path = "hosts"
	ansible.playbook = "playbooks/node2.yaml"
    end
  end
end
