# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    # General configuration
    config.vm.box = "generic/ubuntu2204"
    config.ssh.insert_key = false

    config.vm.provider :virtualbox do |v|
        v.memory = 4096
        v.cpus = 2
        v.linked_clone = true
    end

    # VM configuration
    config.vm.define "ubuntu2204" do |ubuntu2204|
        ubuntu2204.vm.hostname = "dev-box"
    end

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yml"
    end
end