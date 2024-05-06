Vagrant.configure("2") do |config|

  config.vm.define "centos-infra-vm" do |centos1|
    centos1.vm.box = "centos/7"
    # Create a private network
    centos1.vm.network "private_network", ip: "192.168.60.10", name: "vboxnet4"
    # Hostname
    centos1.vm.hostname = "infra.com"

    # Provider-specific configuration
    centos1.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = "2"
      vb.name = "Infra VM 1"
    end
  end
  
end