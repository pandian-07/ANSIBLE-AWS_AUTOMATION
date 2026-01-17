Ansible AWS EC2 Automation Project

📌 Project Overview

This project demonstrates end-to-end automation of AWS EC2 infrastructure using **Ansible**. A single Ansible control node dynamically provisions and configures multiple EC2 instances (managed nodes) in a secure, scalable, and cost-effective way using IAM roles, dynamic inventory, and role-based configuration management.

---

🏗 Architecture

* **Control Node**: EC2 instance with Ansible installed
* **Managed Nodes**: Multiple EC2 instances created dynamically
* **Authentication**: AWS IAM Role attached to control node (no access keys)
* **Networking**: Private IP-based communication

---

⚙️ Technologies Used

* **Cloud**: AWS EC2, IAM
* **Automation**: Ansible
* **OS**: Amazon Linux
* **Web Server**: Apache (HTTPD)
* **Language**: YAML

---

📁 Project Structure

```
ansible-ec2/
├── create-ec2.yml        # Playbook to create EC2 instances
├── inventory.txt         # Dynamic inventory (private IPs)
├── site.yml              # Main playbook to configure servers
├── roles/
│   └── webserver/
│       ├── tasks/main.yml
│       ├── handlers/main.yml
│       ├── templates/index.html.j2
│       ├── vars/main.yml
│       └── defaults/main.yml
└── ansible.cfg
```

---

🚀 Features

* Automated EC2 instance provisioning using Ansible
* Dynamic inventory generation with private IPs
* Role-based HTTPD installation and configuration
* Secure AWS authentication using IAM Roles
* Cost-optimized infrastructure using t2.micro instances

---

▶️ How to Run

1. Attach an IAM role with EC2 permissions to the control node
2. Install Ansible on the control node
3. Update variables in `create-ec2.yml` (AMI, region, instance count)
4. Run the playbook:

   ```bash
   ansible-playbook create-ec2.yml
   ```
5. Configure servers using roles:

   ```bash
   ansible-playbook site.yml
   ```

---

📈 Learning Outcomes

* Practical experience with Infrastructure as Code (IaC)
* Understanding of dynamic inventory and Ansible roles
* Secure and scalable AWS automation practices
* Real-world DevOps workflow implementation

---

📌 Use Case

Suitable for DevOps learners and professionals looking to automate AWS infrastructure provisioning and configuration using Ansible best practices.

---

✨ Author

M Pandian

⭐ If you find this project useful, feel free to star the repository!

