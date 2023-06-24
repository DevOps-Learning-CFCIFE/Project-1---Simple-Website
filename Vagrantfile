Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
    #
    # Forward Port 8080 from vagrant box to Port 8081 on Local
    config.vm.network "forwarded_port", guest: 80, host: 8081
  config.vm.synced_folder "/home/peter/.ssh", "/vagrant"
  config.vm.network "private_network", type: "dhcp"
    #
    #
    # Run Ansible from the Vagrant Host
    #
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.provision "shell", inline: <<-SHELL
    cat /vagrant/id_ed25519.pub >> /home/vagrant/.ssh/authorized_keys
  SHELL
end
