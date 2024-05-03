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

### BD_EPG_Creation

```
cd CiscoACI_Ansible/BD_EPG_Creation/
```


### Varibables
To test the code you have to change the following files:   
- **credentials.yml**: Edit this file with your own APIC URL/Username/Password. If you are doing some test in the Cisco Sandbox, you don't have to edit it
- **data.csv**: Edit this file with your own fabric information. I would liked to review with you all the column in the CSV file:
    - **TENANT**: The Tenant name
    - **VRF**: The VRF name
    - **BD**: The Bridge Domain name
    - **L2_UNKUNICAST**: Enable the L2 Unkown Unicast Flooding [flood]
    - **ARP_FLOODING**: Enable the ARP Flooding [true, false]
    - **ROUTING**: Enable the Unicast Routing flag [true, false]
    - **GW**: IP Address of the Subnet (i.e. "192.168.1.254")
    - **MASK**: Mask of the Subnet (i.e. "24")
    - **GW_PRIMARY**: Enable the "Primary" fuction of the subnet [true, false]
    - **SUBNET_SCOPE**: Specify if the subnet is [private, public]
    - **ANP**: The Application Profile name
    - **EPG**: The EPG name
    - **DOMAIN_TYPE**: The domain type [phys, vmm]
    - **DOMAIN**: The domain name
    - **EPG_PREFERRED**:Enable/Disable the preferred group [disabled, enabled]
    - **EPG_BD_DESCR**: The EPG/BD description, for a network centric migration I usually punt "VLAN - VLAN_ID" --> "VLAN - 10"
    - **PROV_CONTRACT**: The name of the provided contract
    - **CONS_CONTRACT**: The name of the consumer contract

If you want to see an example, open the "simple.csv".

### Run the playbook

After changing the "credentials.yml" and "data.csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```
