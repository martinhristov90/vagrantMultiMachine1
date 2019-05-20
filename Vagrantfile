Vagrant.configure("2") do |config|

    #Creating a loop for provisioning of two machines.
    (1..2).each do |i|
        #Defining each machine.
      config.vm.define vm_name="web#{i}" do |node|
        #Name of the box to be used.
        node.vm.box = "martinhristov90/ubuntu_nginx"
        #Setting hostname for the machine.
        node.vm.hostname = vm_name
        #Forwarding ports to the host machine. First machine is getting 8080 + 1, the second machine is getting port 8080+2.
        node.vm.network "forwarded_port", guest: 80, host: 8080 + i

      end
    end
end
