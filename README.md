## About

The purpose of this repo is to leverage ACI API inspector and turn change deployment into fully stacked API Automation.

## Deployment

1. Populate ***template_variables.xlsx***.
2. Run ***./template_menu.sh*** and paste variables for each function separately, i.e. one run for interface_selector, another run for epg. At the end of the run you'll be presented with an option to lookup the final variable file. This will also place file automatically into ***role/vars folder***.
3. Run ansible-playbook command (more on syntax below).


## Layout
```bash
├── implementation
│   ├── ansible.cfg
│   ├── ap.yml
│   ├── ap.yml_bck
│   ├── bd_subnet.yml
│   ├── bd.yml
│   ├── contract_filter.yml
│   ├── contract.yml
│   ├── epg_contract.yml
│   ├── epg_domain.yml
│   ├── epg_mapping_fex.yml
│   ├── epg_mapping_leaf.yml
│   ├── epg_subnet.yml
│   ├── epg.yml
│   ├── host_vars
│   │   └── sandboxapicdc.cisco.com
│   ├── interface_pg.yml
│   ├── interface_profile_fex.yml
│   ├── interface_profile.yml
│   ├── interface_selector_fex.yml
│   ├── interface_selector.yml
│   ├── interface_to_switch_profile.yml
│   ├── login.yml
│   ├── roles
│   │   ├── ap
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── bd
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── bd_subnet
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── contract
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── filter_backout.yml
│   │   │   │   ├── filter_implement.yml
│   │   │   │   ├── implement.yml
│   │   │   │   ├── main.yml
│   │   │   │   ├── subject_backout.yml
│   │   │   │   └── subject_implement.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── contract_filter
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── entry_backout.yml
│   │   │   │   ├── entry_implement.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── epg
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── epg_contract
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── epg_domain
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── epg_mapping_fex
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── epg_mapping_leaf
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── epg_subnet
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── interface_pg
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── interface_profile
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── interface_profile_fex
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── interface_selector
│   │   │   ├── tasks
│   │   │   │   ├── add_backout.yml
│   │   │   │   ├── add_implement.yml
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── interface_selector_fex
│   │   │   ├── tasks
│   │   │   │   ├── add_backout.yml
│   │   │   │   ├── add_implement.yml
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── interface_to_switch_profile
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   ├── switch_profile
│   │   │   ├── tasks
│   │   │   │   ├── backout.yml
│   │   │   │   ├── implement.yml
│   │   │   │   └── main.yml
│   │   │   ├── templates
│   │   │   │   └── main.j2
│   │   │   └── vars
│   │   │       └── main.yml
│   │   └── vpc
│   │       ├── tasks
│   │       │   ├── backout.yml
│   │       │   ├── implement.yml
│   │       │   └── main.yml
│   │       ├── templates
│   │       │   └── main.j2
│   │       └── vars
│   │           └── main.yml
│   ├── switch_profile.yml
│   ├── template_generator.yml
│   ├── template_list.txt
│   ├── template_menu.sh
│   └── vpc.yml
├── inventories
│   └── inventory.txt
├── README.md
├── requirements.txt
├── template_variables.xlsx
└── vault.txt
```

## Files

The main files are:

1. ***./template.menu.sh*** - copy/paste ***template_variables.xlsx*** spreadsheet's content variables (no headings) and submit with Ctrl+D. This will invoke Jinja template generator that will output the variables in a format Ansible loop statements understand.
2. Run Ansible plays with the following commands:

> ***ansible-playbook ap.yml -i ../inventories/inventory.txt --tags="go"  --vault-password-file ../vault.txt --limit "sandboxapicdc.cisco.com,"***

> ***ansible-playbook ap.yml -i ../inventories/inventory.txt --tags="stop"  --vault-password-file ../vault.txt --limit "sandboxapicdc.cisco.com,"***

Note the tags, they vary dependent if you wish to deploy or rollback configuration. For the available tags explore main Ansible plays and see how they correspond to the respective ***roles/{{ role }}/tasks/main.yml*** files.
You can construct all ansible-playbooks statements into any wrapper of your choice, good example can be found here: ***[Menu_Bash](https://bash.cyberciti.biz/guide/Menu_driven_scripts)***. In addition you can write up mor einteractive script that prompts you for a variety of variables and passes them onto ***--extra-vars (or -e)*** block (i.e. tenant, APIC hostname etc.)
 
## Misc

1. The verificaiton part is not part of plays, further development is required with assert module and CI/CD pipeline i.e. Ansible Tower, GitLab or Jenkins.
2. If you require more roles, just grab API Inspector, mimic required APIC functionality via GUI and grab ready API call for it. Then follow the folder/file patter as above and replace API's variables with ***{{ }}*** of your choice. Add more tabs to the ***.xlxs*** template and you're ready to go. Rememeber template's generator function name = role's name.
3. Tested with number of APICs software versions, but they may vary around API syntax. If you see the errors during the deployment try to run play in verbose mode -vvv for more clues. It may be a case you'll need to re-write API call completely, however the rest of folder/file structure remains the same.
