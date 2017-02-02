# vi: ft=ruby

require 'rbconfig'

VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define 'ftpcentos' do |node|
    node.vm.box = 'bertvv/centos72'
    node.vm.hostname = 'ftpcentos'
    node.vm.network 'private_network', ip: '192.168.56.23'
  end

  config.vm.define 'ftpubuntu' do |node|
    node.vm.box = 'geerlingguy/ubuntu1604'
    node.vm.hostname = 'ftpubuntu'
    node.vm.network 'private_network', ip: '192.168.56.24'
  end

  config.vm.define 'ftpfedora' do |node|
    node.vm.box = 'bertvv/fedora25'
    node.vm.hostname = 'ftpfedora'
    node.vm.network 'private_network', ip: '192.168.56.25'
  end

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'test.yml'
  end
end

