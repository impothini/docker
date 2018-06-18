Vagrant.configure(2) do |config|
  config.hostmanager.enabled = true
  config.hostmanager.ignore_private_ip = false
  config.hostmanager.include_offline = true

  config.vm.define "docker" do |docker|
    config.vm.provider "virtualbox" do |v|
      v.name = "ansible-docker"
    end
    docker.vm.box = "centos/7"
    docker.vm.hostname = "docker.mylab.com"
    docker.vm.network :private_network, ip: "10.0.0.17"
    docker.hostmanager.aliases = %w(docker)
    docker.vm.provision "shell", inline: <<-SHELL
    SHELL
  end

end
