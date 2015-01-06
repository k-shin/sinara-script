# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define :example do |example|
    example.vm.box = "ubuntu-14.04"
    example.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
    example.vm.network "private_network", ip: "192.168.56.2"
    example.vm.network "forwarded_port", guest: 5000, host: 25000, auto_correct: true
    example.vm.provision "ansible" do |ansible|
      ansible.playbook = "sinatra.yml"
    end
  end

end
