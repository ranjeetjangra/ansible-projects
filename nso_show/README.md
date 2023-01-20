***Talk to Cisco IOS device in NSO using Ansible Playbook***

This project is to check the status of Cisco IOS device running connected to Cisco NSO Orchestrator . We use cisco.nso.show_nso ansible galaxy module to communicate with end device.

***Setup Architecture***

![This is an image](https://github.com/ranjeetjangra/ansible-projects/blob/main/nso_show/setup_architecture.png)

***Playbook Running Output***


ranjeet:nso_show$ ansible-playbook nso_show_playbook.yaml --ask-vault-pass
Vault password: 
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [show NSO Data] *************************************************************************************************************

TASK [Gathering Facts] ***********************************************************************************************************
ok: [localhost]

TASK [include_vars] **************************************************************************************************************
ok: [localhost]

TASK [debug] *********************************************************************************************************************
ok: [localhost] => {
    "msg": "Opening URL --- http://192.168.0.141:8080/jsonrpc"
}

TASK [debug] *********************************************************************************************************************
ok: [localhost] => {
    "msg": "admin:admin"
}

TASK [debug] *********************************************************************************************************************
ok: [localhost] => {
    "msg": "{SCSG57-IOSXR0}"
}

TASK [Show admin-state of IOS Device] ********************************************************************************************
ok: [localhost]

TASK [Display the Result] ********************************************************************************************************
ok: [localhost] => {
    "result": {
        "changed": false,
        "failed": false,
        "output": {
            "data": {
                "tailf-ncs:devices": {
                    "device": [
                        {
                            "name": "SCSG57-IOSXR0",
                            "state": {
                                "admin-state": "unlocked"
                            }
                        }
                    ]
                }
            }
        }
    }
}

PLAY RECAP ***********************************************************************************************************************
localhost                  : ok=7    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0 
