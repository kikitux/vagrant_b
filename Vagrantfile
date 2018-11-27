Vagrant.configure("2") do |config|
  
    config.vm.define vm_name="web01" do |node|
      node.vm.network "forwarded_port", guest: 80, host: 8081, auto_correct: true
      node.vm.box = "nikcbg/nginx64"
      node.vm.hostname = vm_name
      node.vm.network "private_network", ip: "192.168.56.56"
    end
  
   config.vm.define vm_name="web02" do |node|
     node.vm.network "forwarded_port", guest: 80, host: 8082, auto_correct: true
     node.vm.box = "nikcbg/nginx64"
     node.vm.hostname = vm_name
     node.vm.network "private_network", ip: "192.168.56.57"
   end
  
end
