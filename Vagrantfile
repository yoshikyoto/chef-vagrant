# coding: utf-8
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  # vagrant box list とかで出てくるやつ
  config.vm.box = "centos/7"
  config.vm.hostname = "vagrant"

  # ホストのポート 8080 をvagrantの80につなげる
  # config.vm.network "forwarded_port", guest: 80, host: 58080

  # ipアドレス ipは適当に変更しておｋ
  config.vm.network :private_network, ip: "192.168.33.12"
  config.ssh.insert_key = false
  config.ssh.forward_agent = true

  # ホストとディレクトリを同期する例
  # config.vm.synced_folder "applications", "/home/vagrant/applications", create: true, mount_options: ["uid=vagrant,gid=vagrant"]

  config.omnibus.chef_version = :latest
end
