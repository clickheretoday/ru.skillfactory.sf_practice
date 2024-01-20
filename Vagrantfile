Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.provision "file", source: "./empty_file", destination: "/home/vagrant/empty_file"
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y python3 python3-pip python3-dev libpq-dev
    pip3 install psycopg2 django
  SHELL
end
