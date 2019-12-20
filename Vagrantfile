Vagrant.configure("2") do |config|
    config.vm.define "m" do |m|
      m.vm.box = "ubuntu/xenial64"
      m.vm.hostname = 'ubuntu'
      #m.disksize.size = '2GB'

      m.vm.network :private_network, ip: "192.168.33.11"
      m.vm.network :forwarded_port, guest: 22, host: 10221, id: "ssh"


      m.vm.provider :virtualbox do |v|
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        v.customize ["modifyvm", :id, "--memory", 512]
        v.customize ["modifyvm", :id, "--name", "m"]
        #v.customize ["modifyhd", "dbba052c-bc41-4416-8a77-3909fc8a5271", "--resize", "2048"]
      end
    end

    config.vm.define "m" do |m|
      m.vm.box = "debian/stretch64"
      m.vm.hostname = 'debian'
      #m.disksize.size = '2GB'

      m.vm.network :private_network, ip: "192.168.33.12"
      m.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"

      m.vm.provider :virtualbox do |v|
        v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        v.customize ["modifyvm", :id, "--memory", 512]
        v.customize ["modifyvm", :id, "--name", "m"]
        #v.customize ["modifyhd", "e1e96847-ea50-491a-bb32-36c9cacc3cf2", "--resize", "2048"]
      end
    end

    config.vm.define "m" do |m|
        m.vm.box = "centos/7"
        m.vm.hostname = 'centos'
        #m.disksize.size = '2GB'

        m.vm.network :private_network, ip: "192.168.33.13"
        m.vm.network :forwarded_port, guest: 22, host: 10223, id: "ssh"

        m.vm.provider :virtualbox do |v|
          v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
          v.customize ["modifyvm", :id, "--memory", 512]
          v.customize ["modifyvm", :id, "--name", "m"]
          #v.customize ["modifyhd", "1bf13eeb-1147-4a50-96e6-ca171fc273fe", "--resize", "2048"]
        end
      end

  end