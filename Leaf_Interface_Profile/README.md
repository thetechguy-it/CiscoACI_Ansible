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

### Leaf_Interface_Profile

```
cd Leaf_Interface_Profile/
```


### Varibables
To test the code you have to change the following files:   
- **credentials.yml**: Edit this file with your own APIC URL/Username/Password. If you are doing some test in the Cisco Sandbox, you don't have to edit it
- **data.csv**: Edit this file with your own fabric information. I would liked to review with you all the column in the CSV file:
  - **name**: The name of the Leaf Interface Profile, here is my tip:
    - **Interface Profile for a Single Leaf (vPC Peer1)**: Leaf-161_IntProf
    - **Interface Profile for a Single Leaf (vPC Peer2)**: Leaf-162_IntProf
    - **Interface Profile for a vPC Domain**: Leaf-161-162_IntProf
  - **description** [Optional]: The policy description

If you want to see an example, open the "simple.csv".

### Run the playbook

After changing the "credentials.yml" and "data.csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```
