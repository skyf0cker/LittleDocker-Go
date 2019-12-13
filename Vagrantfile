# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"
  config.vm.provision "shell", inline: <<-SHELL
    curl -fsSL https://get.docker.com/ | sh
    usermod -aG docker vagrant
    apt-get update
    apt-get dist-upgrade -y
    snap install --classic go
    wget http://dl-cdn.alpinelinux.org/alpine/v3.6/releases/x86_64/alpine-minirootfs-3.6.2-x86_64.tar.gz
    mkdir /var/lib/alpine
    tar -xzvf alpine-minirootfs-3.6.2-x86_64.tar.gz -C /var/lib/alpine
  SHELL
end