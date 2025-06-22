# 🛰️ NetMaze Explorer – Hybrid Networking in Azure
## 📌 Description
A cloud networking project simulating a hybrid on-premises-to-Azure environment using VPN Gateway, Bastion, Private Link, NSGs, and more. Designed to simulate real-world networking scenarios for secure, scalable virtual environments.
## 📸 Screenshots

### 1. Subnet Configuration
Shows five subnets created within `main_vnet`, each with NSGs attached.

![Subnets View](screenshots/01_subnets_view.png)

---

### 2. Site-to-Site VPN Connection
Demonstrates a working connection between `main-vng` and on-prem simulation.

![VPN Connected](screenshots/02_site_to_site_connected.png)

---

### 3. Bastion Login to VM
Confirms Bastion access and internal VM connectivity via SSH.

![Bastion Login](screenshots/03_bastion_login.png)

---

### 4. NSG Web Inbound Rules
Inbound rules for the Web NSG, allowing HTTP and HTTPS traffic.

![NSG Web Rules](screenshots/04_nsg_web_rules.png)

---

### 5. NSG HTTP Rule Detail
Details of the `Allow-HTTP` rule for TCP port 80.

![HTTP Rule](screenshots/05_nsg_http_rule_detail.png)

---

### 6. Private Endpoint for Azure SQL
Validates private link connection to Azure SQL Database with private IP.

![Private Endpoint](screenshots/06_private_endpoint_sql.png)

---

### 7. Ping Test to Web VM
Successful ICMP ping to 10.0.1.4 (vm-web).

![Ping VM Web](screenshots/07_ping_vm_web.png)

---

### 8. Ping Test to DB VM
Successful ping to 10.0.2.4 (vm-db).

![Ping VM DB](screenshots/08_ping_vm_db.png)

## 🔧 Technologies Used
Azure Virtual Network (VNet)

Azure VPN Gateway

Azure Bastion

Azure NSG

Azure Private Endpoint (SQL)

Ubuntu VMs

Azure Resource Manager (ARM) / Portal
## 🗂️ Repo Structure
<pre> NetMaze-Explorer/
├── diagrams/
│   └── netmaze-diagram.png
├── screenshots/
│   └── bastion-ssh.png
│   └── nsg-rules.png
├── notes/
│   └── testing-notes.md
├── README.md
</pre>
## 🧠 What I Learned
How to build secure network topologies in Azure.

Site-to-site VPN configuration and routing concepts.

Using Bastion to securely access VMs with no public IP.

Network security best practices with NSGs and Private Link.

