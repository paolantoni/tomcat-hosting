# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.box = "centos/7"
  config.vm.provision :docker
  config.vm.provision :docker_compose, run: "always", yml: "/vagrant/docker/docker-compose.yml"
  for i in 8000..9000
	config.vm.network "forwarded_port", guest: i, host: i, host_ip: "127.0.0.1" #docker-compose, service: tomcat
  end
 
end
