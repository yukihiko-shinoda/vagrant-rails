Dotenv.load
Vagrant.configure(2) do |config|
  config.vm.box = "futureys/rails"
  config.vm.hostname = "rails"
  config.vm.network :forwarded_port, guest: 80, host: 80
  config.vm.network :forwarded_port, guest: 443, host: 443
  config.vm.network :forwarded_port, guest: 3000, host: 3000
  config.vm.synced_folder "./", "/vagrant", type:"nfs"
  # config.vm.provision "ansible_local" do |ansible|
  #   ansible.playbook = "provisioning/playbook.yml"
  #   ansible.verbose        = "vvv"
  #   ansible.extra_vars = "provisioning/group_vars/default"
  # end
end
