Vagrant.configure("2") do |config|
    config.vm.define "ubuntu" do |ubuntu|
      ubuntu.vm.box = "ubuntu/xenial64"
      ubuntu.vm.hostname = 'ubuntu'

      ubuntu.vm.network :private_network, ip: "192.168.33.11"
      ubuntu.vm.network :forwarded_port, guest: 22, host: 10221, id: "ssh"


      ubuntu.vm.provider :virtualbox do |v|
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        v.customize ["modifyvm", :id, "--memory", 512]
        v.customize ["modifyvm", :id, "--name", "ubuntu"]
      end
    end

    config.vm.define "debian" do |debian|
      debian.vm.box = "debian/stretch64"
      debian.vm.hostname = 'debian'

      debian.vm.network :private_network, ip: "192.168.33.12"
      debian.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"

      debian.vm.provider :virtualbox do |v|
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        v.customize ["modifyvm", :id, "--memory", 512]
        v.customize ["modifyvm", :id, "--name", "debian"]
      end
    end

    config.vm.define "centos" do |centos|
        centos.vm.box = "centos/7"
        centos.vm.hostname = 'centos'

        centos.vm.network :private_network, ip: "192.168.33.13"
        centos.vm.network :forwarded_port, guest: 22, host: 10223, id: "ssh"

        centos.vm.provider :virtualbox do |v|
          v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
          v.customize ["modifyvm", :id, "--memory", 512]
          v.customize ["modifyvm", :id, "--name", "centos"]
        end
      end

  end