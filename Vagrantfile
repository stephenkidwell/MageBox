# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    config.vm.box = "swapnil/magebox"
    config.vm.provider :virtualbox do |vb|
	    vb.customize ["modifyvm", :id, "--memory", "2048"]
	end

    config.vm.network "private_network", ip: "192.168.20.10"
    config.vm.hostname = "magebox"
    config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]
    
    # Optional NFS. Make sure to remove other synced_folder line too
    #config.vm.synced_folder ".", "/var/www", :nfs => { :mount_options => ["dmode=777","fmode=666"] }

end
