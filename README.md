# CCNA Inter-VLAN Routing Enterprise Lab

**CCNA Enterprise Inter-VLAN Routing Lab** | Hierarchical Network Design, VLAN Segmentation, Inter-VLAN Routing, Security, and Real-World Enterprise Simulation

---

## 🌐 Project Overview
This lab simulates a real-world enterprise network, demonstrating:
- Hierarchical design (Core → Distribution → Access layers)
- VLAN segmentation for departments
- Inter-VLAN routing with Layer 3 devices
- Secure management and switch configuration
- Network behavior with STP, VTP, Port Security, and PortFast
- Both IPv4 and IPv6 addressing

Hands-on experience for configuring and managing enterprise switches and routers.

---

## 🏢 Network Topology
- **Hierarchical design:** Core → Distribution → Access
- **VLANs & Departments:**
  - VLAN 10: IT
  - VLAN 20: HR
  - VLAN 30: Finance
  - VLAN 40: Management/Admin
- **Security & Protocols:**
  - SSH for secure management
  - Port Security on access ports
  - Spanning Tree Protocol (STP) for loop prevention
  - VTP for VLAN consistency
  - PortFast on host ports

> ![Topology Diagram](Documentation/12-26-2025 10-24-26 AM.jpg)

---

## 🖧 IP Addressing & Routing

### IPv4 Addresses

| Device       | VLAN | Department        | IP Address     |
|--------------|------|-----------------|---------------|
| SW1:ACCESS   | 10   | IT               | 192.168.10.1  |
| SW1:ACCESS   | 20   | HR               | 192.168.20.1  |
| SW1:ACCESS   | 30   | Finance          | 192.168.30.1  |
| SW1:ACCESS   | 40   | Management/Admin | 192.168.40.1  |
| SW2-DIST     | 10   | IT               | 192.168.10.2  |
| SW2-DIST     | 20   | HR               | 192.168.20.2  |
| SW2-DIST     | 30   | Finance          | 192.168.30.2  |
| SW2-DIST     | 40   | Management/Admin | 192.168.40.2  |
| MSW1:CORE    | 10   | IT               | 192.168.10.3  |
| MSW1:CORE    | 20   | HR               | 192.168.20.3  |
| MSW1:CORE    | 30   | Finance          | 192.168.30.3  |
| MSW1:CORE    | 40   | Management/Admin | 192.168.40.4  |

### IPv6 Addresses

| Device       | VLAN | IPv6 Address          |
|--------------|------|---------------------|
| SW1:ACCESS   | 10   | 2000:AB:CD:10::1    |
| SW1:ACCESS   | 20   | 2000:AB:CD:20::1    |
| SW1:ACCESS   | 30   | 2000:AB:CD:30::1    |
| SW1:ACCESS   | 40   | 2000:AB:CD:40::1    |
| SW2-DIST     | 10   | 2000:AB:CD:10::2    |
| SW2-DIST     | 20   | 2000:AB:CD:20::2    |
| SW2-DIST     | 30   | 2000:AB:CD:30::2    |
| SW2-DIST     | 40   | 2000:AB:CD:40::2    |
| MSW1:CORE    | 10   | 2001:DB8:ACAD:10::3 |
| MSW1:CORE    | 20   | 2001:DB8:ACAD:20::3 |
| MSW1:CORE    | 30   | 2001:DB8:ACAD:30::3 |
| MSW1:CORE    | 40   | 2001:DB8:ACAD:40::3 |

---

## 🔄 Routing Configuration
- Inter-VLAN routing on **Core Switch (MSW1)**
- Enable IP routing (`ip routing`) on Layer 3 switch
- SVIs for each VLAN configured with gateway IP
- Test connectivity using `ping` and `traceroute` (IPv4 & IPv6)

---

## 🔐 Security & Switching Features

**Spanning Tree Protocol (STP)**  
- Prevent Layer 2 loops  
- Rapid PVST+ for fast convergence  
- Root Bridge on Core switch  

**VLAN Trunking Protocol (VTP)**  
- Maintain VLAN consistency  
- Core: Server, Distribution/Access: Clients  

**Port Security**  
- Limit MAC addresses per port  
- Action: Shutdown on violation  

**PortFast**  
- Instant host connectivity  
- Reduces STP delay on Access ports  

---

## 💡 Key Skills Demonstrated
- VLAN creation and configuration  
- Inter-VLAN routing (IPv4 & IPv6)  
- STP, PortFast, VTP, Port Security  
- Secure management via SSH  
- Hierarchical network design  
- Troubleshooting connectivity & security issues  

---

## 📁 Files Included
- `config-files/` → Switches and router configs  
- `Documentation/` → Project images & diagrams  
- `ccna-intervlan-routing-enterprise-lab.pkt` → Packet Tracer file  

---

## ✅ Learning Outcomes
- Apply CCNA-level concepts in enterprise environment  
- Implement secure inter-VLAN communication  
- Configure advanced switching protocols  
- Document configurations professionally  

---

## 🚀 How to Use This Lab
1. Open configurations in Packet Tracer, GNS3, or real devices  
2. Apply VLAN and interface configurations to switches and routers  
3. Test inter-VLAN connectivity (IPv4 & IPv6)  
4. Verify security features (Port Security, SSH) and STP operation  

---

## 🔗 Author
**Eng. Tarek Abdel Aziz** – Network Engineer | Cybersecurity | Python (Networking & Security) | Social Engineering  
- Email: engineertarekabdelaziz@gmail.com  
- Location: Alexandria, Egypt
