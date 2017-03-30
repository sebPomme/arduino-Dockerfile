# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_DEFAULT_PROVIDER'] = 'docker'
ENV['VAGRANT_DEFAULT_PROVISIONER'] = 'docker'
DOCKER_HOST_NAME = "dockerhost"
DOCKER_HOST_VAGRANTFILE = "Docker/Vagrantfile"

Vagrant.configure("2") do |config|
  config.vm.synced_folder ".", Dir.pwd
  config.vm.define "default" do |a|
    a.vm.provider "docker" do |d|
      d.build_dir = "." 
      d.name = "firmiliar"
      d.create_args = [ "--privileged", "-v", "/dev/ttyUSB0:/dev/ttyUSB0" ]
      d.remains_running = false
      d.has_ssh = true
      d.vagrant_machine = "#{DOCKER_HOST_NAME}"
      d.vagrant_vagrantfile = "#{DOCKER_HOST_VAGRANTFILE}"
      d.force_host_vm = true
    end
  end
end
