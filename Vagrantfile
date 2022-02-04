Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.provider "virtualbox" do |vb|
    	vb.name = "elk-host"
    	vb.memory = 4096
    	vb.cpus = 4
    end
    config.vm.network "private_network", ip: "192.168.56.0"
    config.vm.box_download_insecure = true
    config.vm.hostname = "elk-host"
    config.vm.define  "elk-host"
    config.vm.provision  "ansible" do |ansible|
    	ansible.playbook = "setup.yml"
    end
end
    
