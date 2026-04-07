Vagrant.configure("2") do |config|

  #Webserver
  config.vm.define "webserver" do |web|
    web.vm.box = "ubuntu/jammy64"
    web.vm.hostname = "webserver"
    web.vm.network "private_network", ip: "192.168.56.20"

    web.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end

    web.vm.provision "shell", inline: <<-SHELL
  sudo apt update
  sudo apt install -y nginx
  sudo systemctl start nginx
  sudo systemctl enable nginx
  echo "Webserver provisioned successfully by Micah" >> /home/vagrant/provison.log
    SHELL
  end

    #DBserver
  config.vm.define "dbserver" do |db|
    db.vm.box = "ubuntu/jammy64"
    db.vm.hostname = "dbserver"
    db.vm.network "private_network", ip: "192.168.56.21"

    db.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end

    db.vm.provision "shell", inline: <<-SHELL
  sudo apt update
  sudo apt install -y mysql-server
    SHELL
  end

end

