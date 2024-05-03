# CiscoACI_Ansible
In this repository you will find some of Ansible playbooks for common and repetitive Cisco ACI tasks.    
Each folder has an indipendent playbook with relative variable/CSV files, please remember to change credentials and APIC URL each time.
Each folder has 4 files:
- **credentials.yml**: Put here your fabric credentials (URL, Username and Password)
- **main.yml**: This is the code, you don't need to change it. If you want to change it [please check the Module documentation](https://docs.ansible.com/ansible/latest/collections/cisco/aci/index.html)
- **simple.csv**: Here you can find how to modify the "data.csv" file, which is the file that the ansible playbook will use to import the information. se it only as reference.
- **data.csv**: This is the file that you should modify with your leaves/spines/fabric information

Clone the repository to gain access to all the playboooks.    
Enjoy :wink:


# Ansible Installation
To use this repository, you need to install Ansible.   
[Here is the Official installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

# Cisco ACI Ansible Module
For more information about Cisco ACI Ansible Module, [you can find here the Module documentation](https://docs.ansible.com/ansible/latest/collections/cisco/aci/index.html)