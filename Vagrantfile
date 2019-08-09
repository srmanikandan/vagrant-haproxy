Vagrant.configure("2") do |config|
 config.vm.define "lb" do |lb|
  lb.vm.box = "centos/7"
  lb.vm.hostname = "lb.demo.local"
  lb.vm.network :private_network, ip: "172.28.128.10"

  lb.vm.provider :virtualbox do |v|
    v.name = "LB"
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end

  lb.vm.provision :ansible do |deploy|
    deploy.playbook = "scripts/lb.yml"
  end
 end

 config.vm.define "web1" do |web1|
  web1.vm.box = "centos/7"
  web1.vm.hostname = "web1.demo.local"
  web1.vm.network :private_network, ip: "172.28.128.11"

  web1.vm.provider :virtualbox do |v|
    v.name = "web1"
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end

  web1.vm.provision :ansible do |deploy|
    deploy.playbook = "scripts/web.yml"
  end
 end

 config.vm.define "web2" do |web2|
  web2.vm.box = "centos/7"
  web2.vm.hostname = "web2.demo.local"
  web2.vm.network :private_network, ip: "172.28.128.12"

  web2.vm.provider :virtualbox do |v|
    v.name = "web2"
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end

  web2.vm.provision :ansible do |deploy|
    deploy.playbook = "scripts/web.yml"
  end
 end

end
