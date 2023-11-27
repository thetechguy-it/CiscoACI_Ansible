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
- **credentials.yml** : Change the values with your own APIC/Username/Password details. If you want to test the code in the Cisco ACI Sandbox (as per my recommendation), you don't have to change it.
- **epgs_csv** : Change all the values in this CSV file with your own data information.

That's it, nothing more.

If you want to test the code in a virtual environment (from a Linux prospective), please go ahead

### Run the playbook

After changing the "credentials.yml" and "epgs_csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```
