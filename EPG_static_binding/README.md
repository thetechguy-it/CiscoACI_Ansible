# ACI_EPG_static_binding

To test the code you can just clone this repo and change the following files:
- credentials.yml : Change the values with your own APIC/Username/Password details. If you want to test the code in the Cisco ACI Sandbox (as per my recommendation), you don't have to change it.
- epgs_csv : Change all the values in this CSV file with your own data information.

That's it, nothing more.

If you want to test the code in a virtual environment (from a Linux prospective), please go ahead

### Create a virtual environment

```
python3 -m venv ANSIBLE_ACI
source ANSIBLE_ACI/bin/activate
```

### Installing Ansible For Ubuntu/Debian

```
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
cd ANSIBLE_ACI/
```

### Clone the repo

```
git clone git@github.com:thetechguy-it/CiscoACI_Ansible.git
cd CiscoACI_Ansible/EPG_static_binding/
```

### Run the playbook

After changing the "credentials.yml" and "epgs_csv" files, you can run the playbook. I recommend you to test it in the Cisco Sabdbox before pushing in the production:

```
ansible-playbook main.yml
```

### Deactivate the virtual environment

```
deactivate
```