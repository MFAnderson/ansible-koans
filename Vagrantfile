# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = 'ansible1'

  config.vm.provision "ansible" do |ansible|
    ansible.host_key_checking = false
    ansible.playbook = "site.yml"
    ansible.sudo = true
    ansible.limit = 'all'
    ansible.verbose = ''
    ansible.extra_vars = {
        ansible_ssh_user: 'vagrant'
    }
    end
end
