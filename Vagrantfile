# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  NAME = "dev-odoo"
  config.vm.define "odoo" do |odoo|
      odoo.vm.box = "debian7"
      odoo.vm.host_name = NAME

      odoo.vm.synced_folder "~/git/odoo", "/opt/odoo"
      odoo.vm.synced_folder "../addons", "/opt/odoo/.local/share/Odoo/addons/8.0"
      odoo.vm.network :private_network, ip: "192.168.33.2"
      odoo.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--memory", "2048"]
        vb.customize ["modifyvm", :id, "--name", NAME ]
      end
  end
end
