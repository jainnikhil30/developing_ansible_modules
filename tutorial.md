# Quick Tutorial: Creating an Ansible Collection Module

This tutorial guides you through the process of installing Ansible, creating a new Ansible collection, and adding a custom module to it.

## 1. Install Ansible

Use pip to install Ansible:

```bash
pip install ansible
```

## 2. Create an Ansible Collection

Initialize a new collection with the namespace devconf and collection name ansible_workshop. This command sets up the structure for your collection:

```bash
~/.local/bin/ansible-galaxy collection init perfconf.ansible_workshop
```

## 3. Navigate to the Collection Directory
Change to the newly created collection directory:

```bash
cd perfconf/ansible_workshop/
```

## 4. Access the Plugins Directory

Within the collection, navigate to the plugins directory:
```bash
cd plugins/
```

## 5. Create a Modules Directory

Inside the plugins directory, create a directory named modules where your custom modules will reside:
```bash
mkdir modules
```

## 6. Create Your New Module

Move into the modules directory and create a new Python file for your module:
```bash
cd modules
vi userdata.py
```

## 7. Copy the Collection to the Ansible Directory
Finally, copy your collection to the Ansible collections directory:
```bash
cd ~/.ansible
mkdir -p collections/ansible_collections
cd collections/ansible_collections
cp  -r ~/cloudshell_open/developing_ansible_modules/perfconf .
```

Now, let's create a playbook to use the module.
