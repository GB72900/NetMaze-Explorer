# 🛰️ NetMaze Explorer – Hybrid Networking in Azure
## 📌 Description
A cloud networking project simulating a hybrid on-premises-to-Azure environment using VPN Gateway, Bastion, Private Link, NSGs, and more. Designed to simulate real-world networking scenarios for secure, scalable virtual environments.
## 📅 Phase-by-Phase Timeline

| Phase       | Description                                                                                     | Status       |
|-------------|-------------------------------------------------------------------------------------------------|--------------|
| **Phase 1** | Created `main_vnet` with three subnets: WebApp, Admin, and Database                             | ✅ Completed |
| **Phase 2** | Simulated on-premises network with `onprem_vnet` in a separate region                           | ✅ Completed |
| **Phase 3** | Deployed VPN Gateway in `main_vnet` and a Virtual Network Gateway in `onprem_vnet`              | ✅ Completed |
| **Phase 4** | Configured Site-to-Site VPN connection between both VNets and verified connectivity             | ✅ Completed |
| **Phase 5** | Deployed `vm-web`, `vm-admin`, and `vm-db` into respective subnets                               | ✅ Completed |
| **Phase 6** | Applied Network Security Groups (NSGs) to restrict subnet-level traffic                         | ✅ Completed |
| **Phase 7** | Deployed Azure Bastion to securely access VMs over SSH without exposing public IPs              | ✅ Completed |
| **Phase 8** | Attempted to deploy Load Balancer and DNS but was blocked due to free-tier IP quota             | ❌ Skipped   |
| **Phase 9** | Performed security testing and validated private connectivity between subnets                   | ✅ Completed |
| **Phase 10**| Reviewed monitoring options and explored logging features for VPN and NSGs                      | ✅ Completed |

## 📸 Screenshots

### 1. Subnet Configuration
Shows five subnets created within `main_vnet`, each with NSGs attached.
![01_subnets_view](https://github.com/user-attachments/assets/83f1aed2-724a-49d7-9a57-d15f7461b408)


---

### 2. Site-to-Site VPN Connection
Demonstrates a working connection between `main-vng` and on-prem simulation.
![02_site_to_site_connected](https://github.com/user-attachments/assets/6ccbc795-c983-491d-a018-7041e7b2c5cf)


---

### 3. Bastion Login to VM
Confirms Bastion access and internal VM connectivity via SSH.

![03_bastion_login](https://github.com/user-attachments/assets/3843ae9e-2fe6-4e3f-9e3e-8a9a8e709dd4)


---

### 4. NSG Web Inbound Rules
Inbound rules for the Web NSG, allowing HTTP and HTTPS traffic.

![04_nsg_web_rules](https://github.com/user-attachments/assets/d225e081-06de-4751-92c5-7700a76d007b)


---

### 5. NSG HTTP Rule Detail
Details of the `Allow-HTTP` rule for TCP port 80.

![05_nsg_http_rule_detail](https://github.com/user-attachments/assets/173da9bf-7a50-48e1-a768-fee05f0ad334)

---

### 6. Private Endpoint for Azure SQL
Validates private link connection to Azure SQL Database with private IP.

![06_private_endpoint_sql](https://github.com/user-attachments/assets/a2e1cc37-d496-4024-a071-2e9413fcf207)

---

### 7. Ping Test to Web VM
Successful ICMP ping to 10.0.1.4 (vm-web).

![07_ping_vm_web](https://github.com/user-attachments/assets/80cb9750-4dbe-4f56-b00a-bfdfd82702f1)


---

### 8. Ping Test to DB VM
Successful ping to 10.0.2.4 (vm-db).

![08_ping_vm_db](https://github.com/user-attachments/assets/b5feeb0e-68de-401d-9d92-2e8c0f69d315)


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

