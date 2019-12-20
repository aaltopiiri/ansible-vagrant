Vagrant.configure("2") do |config|
    config.vm.define "ubuntu" do |ubuntu|
      ubuntu.vm.box = "ubuntu/xenial64"
      ubuntu.vm.hostname = 'ubuntu'
      #ubuntu.disksize.size = '2GB'

      ubuntu.vm.network :private_network, ip: "192.168.33.11"
      ubuntu.vm.network :forwarded_port, guest: 22, host: 10221, id: "ssh"


      ubuntu.vm.provider :virtualbox do |v|
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        v.customize ["modifyvm", :id, "--memory", 512]
        v.customize ["modifyvm", :id, "--name", "ubuntu"]
        #v.customize ["modifyhd", "dbba052c-bc41-4416-8a77-3909fc8a5271", "--resize", "2048"]
      end
    end

    config.vm.define "debian" do |debian|
      debian.vm.box = "debian/stretch64"
      debian.vm.hostname = 'debian'
      #debian.disksize.size = '2GB'

      debian.vm.network :private_network, ip: "192.168.33.12"
      debian.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"

      debian.vm.provider :virtualbox do |v|
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        v.customize ["modifyvm", :id, "--memory", 512]
        v.customize ["modifyvm", :id, "--name", "debian"]
        #v.customize ["modifyhd", "e1e96847-ea50-491a-bb32-36c9cacc3cf2", "--resize", "2048"]
      end
    end

    config.vm.define "centos" do |centos|
        centos.vm.box = "centos/7"
        centos.vm.hostname = 'centos'
        #centos.disksize.size = '2GB'

        centos.vm.network :private_network, ip: "192.168.33.13"
        centos.vm.network :forwarded_port, guest: 22, host: 10223, id: "ssh"

        centos.vm.provider :virtualbox do |v|
          v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
          v.customize ["modifyvm", :id, "--memory", 512]
          v.customize ["modifyvm", :id, "--name", "centos"]
          #v.customize ["modifyhd", "1bf13eeb-1147-4a50-96e6-ca171fc273fe", "--resize", "2048"]
        end
      end

  end