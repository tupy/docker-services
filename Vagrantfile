# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # https://github.com/tutumcloud/tutum-docker-redis
  config.vm.define "redis" do |redis|
    redis.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "dockerfile/redis"
      d.ports = ["6379:6379"]
      d.name = "redis"
    end
  end

  # https://github.com/tutumcloud/tutum-docker-rabbitmq
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

  # https://github.com/tutumcloud/tutum-docker-mysql
  config.vm.define "mysql" do |mysql|
    mysql.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "tutum/mysql"
      d.name = "mysql"
      d.ports = ["3306:3306"]
    end
  end

  # https://github.com/tutumcloud/tutum-docker-memcached
  config.vm.define "memcached" do |memcached|
    memcached.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "tutum/memcached"
      d.name = "memcached"
      d.ports = ["11211:11211"]
    end
  end


end
