### Clone the repository

To download this code you have to clone the entire repository:

Via HTTPS:

```
git clone https://github.com/thetechguy-it/CiscoACI_Ansible.git
```

Via SSH:

```
git clone git@github.com:thetechguy-it/CiscoACI_Ansible.git
```

### EPG_static_binding

```
cd EPG_static_binding/
```


### Varibables
To test the code you have to change the following files:   
- **credentials.yml**: Edit this file with your own APIC URL/Username/Password. If you are doing some test in the Cisco Sandbox, you don't have to edit it
- **epgs.csv**: Edit this file with your own EPG and port details. I would liked to review with you all the column in the CSV file:
  - **epg**: The name of the EPG
  - **encap_id**: The VLAN ID related to the EPG
  - **ap**: The name of the Application Profile
  - **tenant**: The name of the Tenant
  - **pod_id**: The POD ID
  - **leaf**: The leaves involved:
    - **If the "interface_type" is a vpc**: Put the leaves node ID, like: 101-102
    - **If the "interface_type" is switch_port or port-channel**: Put the leaf node ID, like: 101
  - **interface_type**: The type of the interface. Here are the options:
    - **switch_port**: Single/Access port
    - **port-channel**: Port-Channel (A port channel is an aggregation of multiple physical interfaces that creates a logical interface)
    - **vpc**: Virtual Port-Channel (A virtual port channel (vPC) allows links that are physically connected to two different Cisco Nexus 7000 or 9000 Series devices to appear as a single port channel by a third device)
  - **interface_ipg**: There are two options here:
    - **If the "interface_type" is a vpc or port-channel**: The name of the Interface Policy Group.
    - **If the "interface_type" is switch_port**: The port ID
  - **interface_mode**: The deployment mode of the EPG. Here are the options:
    - **native** or **802.1p**: Use this label if you have a trunk and want to use this EPG as "native".
    - **untagged** or **access**: Use this label if you want to deploy this EPG as untagged in this port/IPG.
    - **tagged**, **regular** or **trunk**: Use this label if you want to deploy this EPG as tagged in this port/IPG.  
- **main.yml**: This is the main code, you don't have to edit it.

That's it, nothing more.

### Run the playbook

After changing the "credentials.yml" and "epgs_csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```
