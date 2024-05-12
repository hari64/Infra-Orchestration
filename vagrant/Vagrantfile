Vagrant.configure("2") do |config|

  config.vm.define "ubuntu-infra-vm1" do |ubuntu1|
    ubuntu1.vm.box = "ubuntu/jammy64"
    # Create a private network
    ubuntu1.vm.network "private_network", type: "dhcp", name: "vboxnet4"
    # Hostname
    ubuntu1.vm.hostname = "infra1"

    # Provider-specific configuration
    ubuntu1.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = "2"
      vb.name = "Infra VM 1"
    end
  end

  config.vm.define "ubuntu-infra-vm2" do |ubuntu2|
    ubuntu2.vm.box = "ubuntu/jammy64"
    # Create a private network
    ubuntu2.vm.network "private_network", type: "dhcp", name: "vboxnet4"
    # Hostname
    ubuntu2.vm.hostname = "infra2"

    # Provider-specific configuration
    ubuntu2.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = "1"
      vb.name = "Infra VM 2"
    end
  end

  config.vm.define "ubuntu-infra-vm3" do |ubuntu3|
    ubuntu3.vm.box = "ubuntu/jammy64"
    # Create a private network
    ubuntu3.vm.network "private_network", type: "dhcp", name: "vboxnet4"
    # Hostname
    ubuntu3.vm.hostname = "infra3"
    #ubuntu3.ssh.username = "vagrant"
    #ubuntu3.ssh.password = "test@env"

    # Provider-specific configuration
    ubuntu3.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = "1"
      vb.name = "Infra VM 3"
    end
  end

end
