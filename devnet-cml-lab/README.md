# README

# Clone this project
```sh
git clone <ssh code URL>
```

# Install the various APT,Python,Galaxy Dependencies

```sh
ansible-playbook install_dependencies.yml
```

```sh
root@ranjeet-VirtualBox:/home/ranjeet/Documents/git-projects/ansible-projects/devnet-cml-lab# ansible-playbook install_dependencies.yml 
[WARNING]: Invalid characters were found in group names but not replaced, use -vvvv to see details

PLAY [Installing Dependencies] *******************************************************************************************************************************************

TASK [Installing Linux APT Dependencies] *********************************************************************************************************************************
ok: [localhost]

TASK [Installing Python PIP Dependencies] ********************************************************************************************************************************
ok: [localhost]

TASK [Installing Galaxy Dependencies] ************************************************************************************************************************************
changed: [localhost]

TASK [Printing Output] ***************************************************************************************************************************************************
ok: [localhost] => {
    "output": {
        "changed": true,
        "cmd": "ansible-galaxy install -r requirements.yml",
        "delta": "0:00:20.449780",
        "end": "2023-02-18 16:41:54.979832",
        "failed": false,
        "msg": "",
        "rc": 0,
        "start": "2023-02-18 16:41:34.530052",
        "stderr": "",
        "stderr_lines": [],
        "stdout": "Starting galaxy collection install process\nProcess install dependency map\nStarting collection install process\n'ansible.netcommon:4.1.0' is already installed, skipping.\n'ansible.utils:2.8.0' is already installed, skipping.\nDownloading https://galaxy.ansible.com/download/community-routeros-2.7.0.tar.gz to /root/.ansible/tmp/ansible-local-27880c34p_yzf/tmpweel6dzw/community-routeros-2.7.0-i0m2jjle\nInstalling 'community.routeros:2.7.0' to '/root/.ansible/collections/ansible_collections/community/routeros'\ncommunity.routeros:2.7.0 was installed successfully",
        "stdout_lines": [
            "Starting galaxy collection install process",
            "Process install dependency map",
            "Starting collection install process",
            "'ansible.netcommon:4.1.0' is already installed, skipping.",
            "'ansible.utils:2.8.0' is already installed, skipping.",
            "Downloading https://galaxy.ansible.com/download/community-routeros-2.7.0.tar.gz to /root/.ansible/tmp/ansible-local-27880c34p_yzf/tmpweel6dzw/community-routeros-2.7.0-i0m2jjle",
            "Installing 'community.routeros:2.7.0' to '/root/.ansible/collections/ansible_collections/community/routeros'",
            "community.routeros:2.7.0 was installed successfully"
        ]
    }
}

PLAY RECAP ***************************************************************************************************************************************************************
localhost                  : ok=4    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
```


# Run main playbook
```sh
ansible-playbook -i inventory.yml main_playbook.yml
```

