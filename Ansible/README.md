# 🛠️ Ansible Commands ..!!
This document contains all essential Ansible commands with short explanations. Useful for beginners and DevOps engineers.

---

## 📁 1. Inventory and Configuration

### Create an inventory file:
```ini
[web]
server1 ansible_host=192.168.1.10 ansible_user=ubuntu

[db]
server2 ansible_host=192.168.1.11 ansible_user=ubuntu
```

### Check Ansible version:
```bash
ansible --version
```

### Ping all hosts:
```bash
ansible all -m ping -i inventory
```

---

## 📦 2. Ad-Hoc Commands

### Run a command on all hosts:
```bash
ansible all -a "uptime" -i inventory
```

### Use modules like `yum`, `apt`, `copy`, `file`, `service`:
```bash
ansible web -m yum -a "name=httpd state=present" -i inventory
ansible web -m service -a "name=httpd state=started" -i inventory
```

### Copy file to remote server:
```bash
ansible all -m copy -a "src=./file.txt dest=/tmp/file.txt" -i inventory
```

### Set permissions on a file:
```bash
ansible all -m file -a "path=/tmp/file.txt mode=0644" -i inventory
```

---

## 📜 3. Playbook Commands

### Run a playbook:
```bash
ansible-playbook site.yml -i inventory
```

### Run a playbook with extra variables:
```bash
ansible-playbook deploy.yml -i inventory -e "version=1.2"
```

### Check (dry run) mode:
```bash
ansible-playbook site.yml -i inventory --check
```

### Limit execution to one host:
```bash
ansible-playbook site.yml -i inventory --limit "server1"
```

---

## 🧰 4. Roles and Galaxy

### Create a new role:
```bash
ansible-galaxy init myrole
```

### Install role from Galaxy:
```bash
ansible-galaxy install geerlingguy.apache
```

---

## 🔐 5. SSH Key and Vault

### Use private SSH key:
```bash
ansible-playbook site.yml -i inventory --private-key ~/.ssh/id_rsa
```

### Create encrypted secret file:
```bash
ansible-vault create secrets.yml
```

### Edit encrypted file:
```bash
ansible-vault edit secrets.yml
```

### Run playbook with vault password:
```bash
ansible-playbook site.yml --ask-vault-pass
```

---

## 🧪 6. Debug and Testing

### Add debug info in playbook:
```yaml
- debug:
    var: my_variable
```

### Print message:
```yaml
- debug:
    msg: "Deployment started"
```

---

## 🧹 7. Common Modules Summary

| Module      | Purpose                        |
|-------------|--------------------------------|
| ping        | Test connection                |
| command     | Run a command                  |
| shell       | Run shell commands             |
| yum/apt     | Install packages               |
| service     | Manage services                |
| file        | Manage file permissions        |
| copy        | Copy files to remote machine   |
| template    | Jinja2 templating              |
| user        | Create/manage users            |
| debug       | Print debug messages           |

---

## 📌 Example Playbook

```yaml
- name: Install and start Apache
  hosts: web
  become: yes
  tasks:
    - name: Install Apache
      apt:
        name: apache2
        state: present

    - name: Start Apache
      service:
        name: apache2
        state: started
```

---

## 🏁 Useful Tips

- Use `-i inventory` to specify your inventory file.
- Use `--limit` to run on specific host/groups.
- Use `--check` for dry-run.
- Use `--tags` and `--skip-tags` to run selected tasks.

---
![Ansible Logo](https://github.com/ansible/logos/blob/main/community-usage/correct-use-white.png)  
*A comprehensive guide to mastering Ansible for DevOps Engineers*

---

## 📚 Overview

Welcome to **Ansible Zero to Hero**, your one-stop resource for learning and mastering Ansible! Whether you're a beginner or an experienced DevOps engineer, this repository has everything you need to automate your infrastructure with Ansible.

This guide covers:

- **Installation**: Step-by-step instructions for getting Ansible up and running.
- **Hosts Configuration**: How to set up and manage your inventory.
- **Ad-Hoc Commands**: Quick and powerful commands for one-time tasks.
- **Playbooks**: Automate complex tasks with reusable Ansible playbooks.
- **Real-World Examples**: Practical examples to help you apply what you've learned.

---
