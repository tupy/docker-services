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

  # https://github.com/tutumcloud/tutum-docker-mongodb
  config.vm.define "mongodb" do |mongodb|
    mongodb.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "tutum/mongodb"
      d.name = "mongodb"
      d.ports = ["27017:27017"]
    end
  end

  # https://github.com/tutumcloud/tutum-docker-elasticsearch
  config.vm.define "elasticsearch" do |elasticsearch|
    elasticsearch.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "tutum/elasticsearch"
      d.name = "elasticsearch"
      d.ports = ["9200:9200"]
    end
  end

  # https://github.com/tutumcloud/tutum-docker-influxdb
  config.vm.define "influxdb" do |influxdb|
    influxdb.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./boot2docker/Vagrantfile"
      d.image = "tutum/influxdb"
      d.name = "influxdb"
      d.ports = ["8083:8083","8086:8086","8090:8090","8099:8099"]
    end
  end


end
