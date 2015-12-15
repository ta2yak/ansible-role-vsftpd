# vi: ft=ruby

require 'rbconfig'

VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define 'ftpcentos' do |node|
    node.vm.box = 'bertvv/centos71'
    node.vm.hostname = 'ftpcentos'
  end

  config.vm.define 'ftpubuntu' do |node|
    node.vm.box = 'ubuntu/trusty64'
    node.vm.hostname = 'ftpubuntu'
  end

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'test.yml'
  end
end

