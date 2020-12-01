Vagrant.configure("2") do |config|
config.vm.define :firewall1 do |firewall1|
 firewall1.vm.box = "bento/centos-7"
 firewall1.vm.network :private_network, ip: "209.191.50.3"
 firewall1.vm.network :public_network, bridge: "Realtek 8822CE Wireless LAN 802.11ac PCI-E NIC", ip: "192.168.10.29"
 firewall1.vm.provision "shell", path: "firewallscript.sh"
 firewall1.vm.hostname = "firewall"
 end
config.vm.define :servidorSTRM do |servidorSTRM|
 servidorSTRM.vm.box = "bento/centos-7"
#servidorSTRM.vm.network :public_network, bridge: "Realtek 8822CE Wireless LAN 802.11ac PCI-E NIC", ip: "192.168.10.30"
 servidorSTRM.vm.network :private_network, ip: "192.168.50.2"
 servidorSTRM.vm.provision "shell", path: "stream.sh"
 servidorSTRM.vm.hostname = "servidorSTRM"
 end
end