```bash
Paste CSV file content and finish with Ctrl+D
common  ap_1    epg_1   default bd_192.168.1.256/24     null
common  ap_2    epg_2   default bd_192.168.2.0/24       null
common  ap_3    epg_3   default bd_192.168.3.0/24       null
 [WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'


PLAY [localhost] ****************************************************************************************************************************************************************************************************************************

TASK [Parse CSV To YAML] ********************************************************************************************************************************************************************************************************************
ok: [localhost]

TASK [Call variables] ***********************************************************************************************************************************************************************************************************************
ok: [localhost]

TASK [Syntax checker - Tenant existence] ****************************************************************************************************************************************************************************************************
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_1', 'name': 'epg_1', 'description': 'default', 'bd': 'bd_192.168.1.256/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_1",
        "bd": "bd_192.168.1.256/24",
        "description": "default",
        "name": "epg_1",
        "tenant": "common"
    },
    "msg": "Tenant defined"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_2', 'name': 'epg_2', 'description': 'default', 'bd': 'bd_192.168.2.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_2",
        "bd": "bd_192.168.2.0/24",
        "description": "default",
        "name": "epg_2",
        "tenant": "common"
    },
    "msg": "Tenant defined"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_3', 'name': 'epg_3', 'description': 'default', 'bd': 'bd_192.168.3.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_3",
        "bd": "bd_192.168.3.0/24",
        "description": "default",
        "name": "epg_3",
        "tenant": "common"
    },
    "msg": "Tenant defined"
}

TASK [Syntax checker - Tenant "common" existience] ******************************************************************************************************************************************************************************************
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_1', 'name': 'epg_1', 'description': 'default', 'bd': 'bd_192.168.1.256/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_1",
        "bd": "bd_192.168.1.256/24",
        "description": "default",
        "name": "epg_1",
        "tenant": "common"
    },
    "msg": "Tenant common defined"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_2', 'name': 'epg_2', 'description': 'default', 'bd': 'bd_192.168.2.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_2",
        "bd": "bd_192.168.2.0/24",
        "description": "default",
        "name": "epg_2",
        "tenant": "common"
    },
    "msg": "Tenant common defined"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_3', 'name': 'epg_3', 'description': 'default', 'bd': 'bd_192.168.3.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_3",
        "bd": "bd_192.168.3.0/24",
        "description": "default",
        "name": "epg_3",
        "tenant": "common"
    },
    "msg": "Tenant common defined"
}

TASK [Syntax checker - BD Subnet /24 existience] ********************************************************************************************************************************************************************************************
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_1', 'name': 'epg_1', 'description': 'default', 'bd': 'bd_192.168.1.256/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_1",
        "bd": "bd_192.168.1.256/24",
        "description": "default",
        "name": "epg_1",
        "tenant": "common"
    },
    "msg": "BD /24 existient"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_2', 'name': 'epg_2', 'description': 'default', 'bd': 'bd_192.168.2.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_2",
        "bd": "bd_192.168.2.0/24",
        "description": "default",
        "name": "epg_2",
        "tenant": "common"
    },
    "msg": "BD /24 existient"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_3', 'name': 'epg_3', 'description': 'default', 'bd': 'bd_192.168.3.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_3",
        "bd": "bd_192.168.3.0/24",
        "description": "default",
        "name": "epg_3",
        "tenant": "common"
    },
    "msg": "BD /24 existient"
}

TASK [Syntax checker - App Profile name] ****************************************************************************************************************************************************************************************************
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_1', 'name': 'epg_1', 'description': 'default', 'bd': 'bd_192.168.1.256/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_1",
        "bd": "bd_192.168.1.256/24",
        "description": "default",
        "name": "epg_1",
        "tenant": "common"
    },
    "msg": "App profile syntax correct"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_2', 'name': 'epg_2', 'description': 'default', 'bd': 'bd_192.168.2.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_2",
        "bd": "bd_192.168.2.0/24",
        "description": "default",
        "name": "epg_2",
        "tenant": "common"
    },
    "msg": "App profile syntax correct"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_3', 'name': 'epg_3', 'description': 'default', 'bd': 'bd_192.168.3.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_3",
        "bd": "bd_192.168.3.0/24",
        "description": "default",
        "name": "epg_3",
        "tenant": "common"
    },
    "msg": "App profile syntax correct"
}

TASK [Syntax checker - EPG Profile name] ****************************************************************************************************************************************************************************************************
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_1', 'name': 'epg_1', 'description': 'default', 'bd': 'bd_192.168.1.256/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_1",
        "bd": "bd_192.168.1.256/24",
        "description": "default",
        "name": "epg_1",
        "tenant": "common"
    },
    "msg": "EPG profile syntax correct"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_2', 'name': 'epg_2', 'description': 'default', 'bd': 'bd_192.168.2.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_2",
        "bd": "bd_192.168.2.0/24",
        "description": "default",
        "name": "epg_2",
        "tenant": "common"
    },
    "msg": "EPG profile syntax correct"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_3', 'name': 'epg_3', 'description': 'default', 'bd': 'bd_192.168.3.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_3",
        "bd": "bd_192.168.3.0/24",
        "description": "default",
        "name": "epg_3",
        "tenant": "common"
    },
    "msg": "EPG profile syntax correct"
}

TASK [Syntax checker - BD name] *************************************************************************************************************************************************************************************************************
failed: [localhost] (item={'tenant': 'common', 'app_prof': 'ap_1', 'name': 'epg_1', 'description': 'default', 'bd': 'bd_192.168.1.256/24'}) => {
    "assertion": "item.bd | regex_search('^bd\\_(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\/24')",
    "changed": false,
    "evaluated_to": false,
    "item": {
        "app_prof": "ap_1",
        "bd": "bd_192.168.1.256/24",
        "description": "default",
        "name": "epg_1",
        "tenant": "common"
    },
    "msg": "BD profile syntax not correct"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_2', 'name': 'epg_2', 'description': 'default', 'bd': 'bd_192.168.2.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_2",
        "bd": "bd_192.168.2.0/24",
        "description": "default",
        "name": "epg_2",
        "tenant": "common"
    },
    "msg": "BD profile syntax correct"
}
ok: [localhost] => (item={'tenant': 'common', 'app_prof': 'ap_3', 'name': 'epg_3', 'description': 'default', 'bd': 'bd_192.168.3.0/24'}) => {
    "changed": false,
    "item": {
        "app_prof": "ap_3",
        "bd": "bd_192.168.3.0/24",
        "description": "default",
        "name": "epg_3",
        "tenant": "common"
    },
    "msg": "BD profile syntax correct"
}
...ignoring

PLAY RECAP **********************************************************************************************************************************************************************************************************************************
localhost                  : ok=8    changed=0    unreachable=0    failed=0


Do you wish to see variable file now? Yy/Nn: y
---
epg:
 - {tenant: "common", app_prof: "ap_1", name: "epg_1", description: "default", bd: "bd_192.168.1.256/24"}
 - {tenant: "common", app_prof: "ap_2", name: "epg_2", description: "default", bd: "bd_192.168.2.0/24"}
 - {tenant: "common", app_prof: "ap_3", name: "epg_3", description: "default", bd: "bd_192.168.3.0/24"}

```
