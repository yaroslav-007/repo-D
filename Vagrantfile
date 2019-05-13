Vagrant.configure("2") do |config|

  # create two web servers with 2 CPUs and 2 GB of RAM
  (1..2).each do |i|
    config.vm.define "web#{i}" do |node|
      node.vm.box = "vatman/nginx64"
      node.vm.hostname = "web#{i}"
        node.vm.provider "virtualbox" do |vb|
            vb.memory = "2048"
            vb.cpus   = "2"
        end
    end 
 end




# create database 
 config.vm.define "db01" do |db|
    db.vm.box = "vatman/mysql64"
    db.vm.hostname = "db01"
 end
end





