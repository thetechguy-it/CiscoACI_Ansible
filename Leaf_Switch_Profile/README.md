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

### Leaf_Switch_Profile

```
cd Leaf_Switch_Profile/
```


### Varibables
To test the code you have to change the following files:   
- **credentials.yml**: Edit this file with your own APIC URL/Username/Password. If you are doing some test in the Cisco Sandbox, you don't have to edit it
- **data.csv**: Edit this file with your own fabric information. I would liked to review with you all the column in the CSV file:
    - **leaf_interface_profile**: The Leaf Interface Profile policy name
    - **leaf_profile**: The Leaf Switch Profile policy name
    - **leaf_profile_descr**: The Leaf Switch Profile policy description
    - **leaf_selector**: The Leaf Switch Selector policy name
    - **Switch1_ID**: The Node ID of the first Switch
    - **Switch2_ID**: The Node ID of the second Switch
    - **policy_group**: The name of the Leaf Policy Group
    - **policy_group_exist**: Depending on your environment, you want or you would not want to create this policy:
        - **no**: Create the policy in the "policy_group" field
        - **yes**: Skip and do not override the policy
    - **switch_type**: You can choose between:
        - **leaf**: If the Profile is for a Leaf
        - **spine**: If the Profile is for a Spine

If you want to see an example, open the "simple.csv".

### Run the playbook

After changing the "credentials.yml" and "data.csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```
