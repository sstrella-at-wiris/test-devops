Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-24.04"
    config.vm.hostname = "test.local"
    config.vm.network :forwarded_port, guest: 80, host: 8080
    config.vm.synced_folder "./src", "/var/srv/test", 
    owner: 'vagrant', group: 'vagrant', mount_options: ["dmode=777", "fmode=777"]
    config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = 2
        vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
    config.ssh.password = "vagrant"
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "provisioning/playbook.yml"
        ansible.extra_vars = {
            app_name: "test",
            app_env: "development",
        }
    end
end