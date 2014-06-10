# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "redis" do |redis|
    redis.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "dockerfile/redis"
      d.ports = ["6379:6379"]
      d.name = "redis"
    end
  end

  config.vm.define "rabbitmq" do |rabbitmq|
    rabbitmq.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "tutum/rabbitmq"
      d.name = "rabbitmq"
      d.ports = ["5672:5672", "15672:15672"]
      d.env = {
        'RABBITMQ_PASS' => 'rabbitmq'
      }
    end
  end

  config.vm.define "mysql" do |mysql|
    mysql.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "tutum/mysql"
      d.name = "mysql"
      d.ports = ["3306:3306"]
    end
  end

end
