servers=[
  {
    :hostname => "vagrant-box-host-1",
    :ip => "192.168.56.11",
    :box => "ubuntu-box",
    :ram => 1024,
    :cpu => 1,
    :ssh_port => 2001
  },
  {
    :hostname => "vagrant-box-host-2",
    :ip => "192.168.56.12",
    :box => "ubuntu-box",
    :ram => 1024,
    :cpu => 1,
    :ssh_port => 2002
  }
]

Vagrant.configure(2) do |config|
    servers.each do |machine|
        config.vm.define machine[:hostname] do |node|
            node.vm.box = machine[:box]
            node.vm.hostname = machine[:hostname]
            node.vm.network "public_network", ip: machine[:ip]
            node.vm.provider "virtualbox" do |vb|
                config.vm.network :forwarded_port, guest: 22, host: machine[:ssh_port], id: "ssh"
	            	config.ssh.username = "labs"
                config.ssh.private_key_path = "labs_private"

                vb.customize ["modifyvm", :id, "--memory", machine[:ram]]
            end
        end
    end
end
