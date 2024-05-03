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

### vPC_Domains

```
cd vPC_Domains/
```


### Varibables
To test the code you have to change the following files:   
- **credentials.yml**: Edit this file with your own APIC URL/Username/Password. If you are doing some test in the Cisco Sandbox, you don't have to edit it
- **data.csv**: Edit this file with your own fabric information. I would liked to review with you all the column in the CSV file:
    - **vPC_Domain_Name**: The vPC Domain policy name
    -**vPC_ID**: The ID of your vPC Domain. Usually I put the lowest ID between the two vPC peers
    - **vPC_Switch1_ID**: The Node ID of the first Switch
    - **vPC_Switch2_ID**: The Node ID of the second Switch

If you want to see an example, open the "simple.csv".

### Run the playbook

After changing the "credentials.yml" and "data.csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```
