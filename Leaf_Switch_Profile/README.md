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


### Run the playbook

After changing the "credentials.yml" and "data.csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```
