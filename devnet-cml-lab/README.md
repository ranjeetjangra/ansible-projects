# README

# Clone this project
```sh
git clone <ssh code URL>
```

# Install the galaxy modules from requirement file

```sh
ansible-galaxy install -r requirements.yml
```

```sh
Starting galaxy collection install process
Process install dependency map
Starting collection install process
Downloading https://galaxy.ansible.com/download/ansible-netcommon-4.1.0.tar.gz to /home/ranjeet/.ansible/tmp/ansible-local-40914m5zg67x/tmpuzntij4i/ansible-netcommon-4.1.0-fwkk8rk2
Installing 'ansible.netcommon:4.1.0' to '/home/ranjeet/.ansible/collections/ansible_collections/ansible/netcommon'
Downloading https://galaxy.ansible.com/download/ansible-utils-2.9.0.tar.gz to /home/ranjeet/.ansible/tmp/ansible-local-40914m5zg67x/tmpuzntij4i/ansible-utils-2.9.0-4iqbalo9
ansible.netcommon:4.1.0 was installed successfully
Installing 'ansible.utils:2.9.0' to '/home/ranjeet/.ansible/collections/ansible_collections/ansible/utils'
ansible.utils:2.9.0 was installed successfully
```

# Run main playbook
```sh
ansible-playbook -i inventory.yml main_playbook.yml
```

