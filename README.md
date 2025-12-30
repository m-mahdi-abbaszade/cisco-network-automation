# 🚀 Cisco Network Automation with Ansible

**Automated Cisco Switch Configuration** – Production-ready, modular, and perfect for NetDevOps interviews!

This repository demonstrates real-world network automation using Ansible to configure Cisco IOS switches.  
Everything is built with clean roles, idempotent playbooks, and best practices — exactly what companies look for in Network Automation and DevOps roles.

## ✨ Features
- Base Configuration (Hostname, NTP, Logging, Banner, Local Admin)
- VLAN Creation & Port Assignment (Access + Trunk ports with descriptions)
- Advanced Interface Configuration (Speed, Duplex, Loopback, Port status)
- Security Hardening  
  → Port Security (Sticky MAC, Violation Restrict)  
  → Storm Control  
  → AAA Authentication (TACACS+ fallback to local)  
  → Service Password-Encryption
- Full modular roles & separate playbooks for easy reuse
- Dev/Prod inventory support
- Automatic config save after every change

## 🏗️ Project Structure
cisco-network-automation/
├── inventories/          # dev & prod hosts
├── group_vars/           # global variables
├── playbooks/            # base, vlan, interface, security, full-deploy
├── roles/                # cisco_base, cisco_vlans, cisco_interfaces, cisco_security
├── ansible.cfg           # optimized for Cisco IOS
└── README.md


## 🚀 Quick Start
1. Clone the repo  
   `git clone git@github.com:m-mahdi-abbaszade/cisco-network-automation.git && cd cisco-network-automation`

2. Update `inventories/dev/hosts.yml` with your switch IP, username, and password

3. Run full deployment  
   `ansible-playbook -i inventories/dev/hosts.yml playbooks/full-deploy.yml`

4. Watch your Cisco switches get configured automatically!

## 🎯 Individual Playbooks
```bash
ansible-playbook -i inventories/dev/hosts.yml playbooks/base-config.yml
ansible-playbook -i inventories/dev/hosts.yml playbooks/vlan-config.yml
ansible-playbook -i inventories/dev/hosts.yml playbooks/interface-config.yml
ansible-playbook -i inventories/dev/hosts.yml playbooks/security-config.yml
```
## 🔒 Security Note
Passwords are stored in plain text for demo purposes.
In production, use Ansible Vault or AWX/Tower.
## 🤝 Contributing
Pull requests are welcome! Feel free to open an issue or submit improvements.
## 📝 Author
Mahdi Abbaszade
Network Automation | DevOps | NetDevOps
LinkedIn: linkedin.com/in/m-mahdi-abbaszade
## ⭐ If you like this project, please give it a Star!
It helps me reach more Network & DevOps professionals.
#NetworkAutomation #Ansible #Cisco #NetDevOps #DevOps #Automation #Networking
