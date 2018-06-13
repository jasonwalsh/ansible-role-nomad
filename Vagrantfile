Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.network "forwarded_port", guest: 4646, host: 4646

  config.vm.provision "ansible" do |ansible|
    ansible.extra_vars = {
      ansible_python_interpreter: "/usr/bin/python3"
    }
    ansible.playbook = "tests/test.yml"
  end
end
