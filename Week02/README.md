# Week 2 Portfolio Project: Enterprise Infrastructure Planning for a Startup Company

**Course:** ITEP 414 – System Administration and Maintenance  
**Institution:** Laguna State Polytechnic University[cite: 1]  
**Prepared By:** Jaypee Rabie  
**Instructor:** John Randolf M. Peñaredondo, MIT[cite: 1]  

---

## Executive Summary
This document outlines the initial end-to-end IT Infrastructure Plan for **ABC Startup Solutions**, a newly established software development firm[cite: 1]. Starting from a zero-equipment baseline, this proposal establishes a reliable, secure, and scalable local area network (LAN), server architecture, hardware deployment strategy, and administrative security framework[cite: 1].

---

## Project Overview & Objectives
The primary objective of this project is to analyze business requirements and build an enterprise-grade IT infrastructure layout from scratch[cite: 1]. 

### Knowledge Objectives
* Understand core operational roles and responsibilities of System Administrators[cite: 1].
* Identify hardware, software, and networking needs for small-to-medium enterprise (SME) startups[cite: 1].
* Apply proper IT documentation and infrastructure planning standards[cite: 1].

### Skill Objectives
* Formulate hardware and software allocation models across business units[cite: 1].
* Structure enterprise asset inventories and network topologies[cite: 1].
* Implement technical documentation standards using clean Markdown[cite: 1].

---

## PART 1: Company Profile[cite: 1]

* **Company Name:** ABC Startup Solutions[cite: 1]
* **Nature of Business:** Software Development, Custom Web Apps, and Mobile Solutions[cite: 1]
* **Office Location:** 4th Floor, Axis IT Tower, Santa Cruz, Laguna, Philippines
* **Vision:** To become a premier software innovation hub delivering secure, scalable, and modern digital platforms for Southeast Asian enterprises.
* **Mission:** To empower businesses through high-quality custom software solutions while fostering a modern, secure, and highly efficient technical workspace for our engineers and operational teams.

### Organizational Structure & Employee Distribution[cite: 1]

| Department | Headcount | Key Responsibilities |
| :--- | :---: | :--- |
| **Information Technology** | 5 | Software Engineering, System Administration, DevOps, QA[cite: 1] |
| **Human Resources** | 4 | Recruitment, Employee Relations, Payroll Coordination[cite: 1] |
| **Finance** | 5 | Financial Accounting, Purchasing, Budgeting, Billing[cite: 1] |
| **Sales & Marketing** | 6 | Business Development, Client Relations, Product Demos[cite: 1] |
| **TOTAL** | **20** | **Single Floor Operations**[cite: 1] |

---

## PART 2: Enterprise Hardware Inventory[cite: 1]

| Asset ID | Hardware Item | Qty | Department | Purpose & Hardware Justification |
| :--- | :--- | :---: | :--- | :--- |
| **HW-DESK-01** | Workstation Desktops (Core i7, 32GB RAM, 1TB NVMe SSD) | 5 | IT | High performance required for local builds, Docker containers, and running virtualized test beds. |
| **HW-DESK-02** | Office Desktops (Core i5, 16GB RAM, 512GB SSD) | 9 | HR (4), Finance (5) | Reliable processing speed for spreadsheet calculations, payroll processing, and HRIS systems. |
| **HW-LAP-01** | Commercial Laptops (Core i5, 16GB RAM, 512GB SSD) | 6 | Sales | Lightweight mobility for field client presentations, sales demos, and remote meetings. |
| **HW-SRV-01** | Rackmount Server (Dell PowerEdge R450, 64GB RAM, 2x2TB SAS RAID 1) | 1 | IT / Central | Hosts local LDAP/Active Directory, internal Git mirrors, local staging builds, and file services. |
| **HW-NAS-01** | Synology 4-Bay NAS (4x4TB HDD, RAID 10 configuration) | 1 | Central | Centralized redundant file storage, automated incremental workstation backups, and document archives. |
| **HW-BUP-01** | External Hard Drive 6TB USB 3.2 | 2 | IT / Central | Offsite physical cold-backup rotation (swapped weekly) following 3-2-1 backup compliance. |
| **HW-MON-01** | 27" Dual Monitor Setup | 10 | IT (5 pairs) | Dual screen real estate to increase coding efficiency, debugging, and system monitoring. |
| **HW-MON-02** | 24" Single Monitor Setup | 15 | HR, Finance, Sales | Standard display for productivity apps, CRM systems, and daily desk operations. |
| **HW-PRN-01** | Enterprise Network Laser Multifunction Printer | 1 | Shared | Centralized duplex printing, document scanning, and copying via network cable. |
| **HW-UPS-01** | 3000VA Rackmount UPS | 1 | Server Room | Provides battery backup and surge protection to server, core switch, router, and NAS during outages. |
| **HW-UPS-02** | 650VA Desktop UPS | 14 | Workstations | Gives desktop users 5-10 minutes to save active work and gracefully shut down during blackouts. |

---

## PART 3: Enterprise Software Inventory[cite: 1]

| Software Name | Version | License Type | Department Assignment | Operational Purpose & Need |
| :--- | :--- | :--- | :--- | :--- |
| **Windows 11 Pro** | 23H2 | Commercial OEM / Volume | All Workstations | Standard OS providing domain join capabilities, BitLocker encryption, and remote desktop access[cite: 1]. |
| **Ubuntu Server** | 24.04 LTS | Open Source (Free) | Server (Dell R450) | Enterprise Linux OS hosting internal services, SSH, Docker engines, and deployment environments[cite: 1]. |
| **Microsoft 365** | Business Standard | SaaS Subscription | All Employees | Essential suite for enterprise email (Exchange), spreadsheets, documentation, and Teams collaboration[cite: 1]. |
| **VS Code** | Latest | Open Source (Free) | IT Department | Primary lightweight Integrated Development Environment (IDE) for software engineering teams[cite: 1]. |
| **Git** | 2.x | Open Source (Free) | IT Department | Distributed version control system required for source code management[cite: 1]. |
| **GitHub Desktop** | Latest | Open Source (Free) | IT Department | GUI client easing Git workflows, code reviews, and local repo tracking for developers[cite: 1]. |
| **VirtualBox** | 7.x | Open Source (GPL v3) | IT Department | Hypervisor allowing developers to spin up isolated Linux environments and testing nodes[cite: 1]. |
| **Google Chrome** | Latest | Freeware | All Employees | Primary secure web browser for cloud SaaS tools, CRM access, and internal web applications[cite: 1]. |
| **Microsoft Defender** | Business Edition | Cloud Managed / Commercial | All Endpoints | Integrated endpoint detection and response (EDR), real-time scanning, and malware protection[cite: 1]. |
| **AnyDesk** | Enterprise | Commercial License | IT Department | Secure remote assistance tool allowing IT staff to troubleshoot remote/sales laptops safely[cite: 1]. |
| **7-Zip** | Latest | Open Source (GNU LGPL) | All Employees | File archiver utility for compressing project deliverables and extracting compressed files[cite: 1]. |

---

## PART 4: Enterprise Network Inventory[cite: 1]

| Network Equipment | Brand / Model | Qty | Specification / Purpose |
| :--- | :--- | :---: | :--- |
| **ISP Modem** | Fiber ONU Modem | 1 | Demarcation point converting fiber optic signal from primary ISP to Ethernet interface[cite: 1]. |
| **Router** | MikroTik RouterBOARD RB4011 | 1 | Handles WAN connections, NAT, inter-VLAN routing, and DHCP pool allocation across departments[cite: 1]. |
| **Firewall Appliance** | pfSense Netgate 4100 | 1 | Enterprise edge security filtering inbound/outbound traffic, intrusion prevention, and SSL-VPN access[cite: 1]. |
| **Managed Switch** | Cisco Catalyst 2960-X (48-Port GbE PoE+) | 1 | Core switch providing VLAN tagging, Port Security, and Power over Ethernet (PoE) for Access Points[cite: 1]. |
| **Wireless Access Point** | Ubiquiti Unifi AP AC Pro | 2 | Dual-band Wi-Fi APs ceiling-mounted for seamless sales laptop access and guest wireless isolation[cite: 1]. |
| **Patch Panel** | 24-Port Cat6 Wall Rackmount | 2 | Terminates all structured Ethernet runs cleanly inside the server cabinet before connecting to the switch[cite: 1]. |
| **CAT6 Ethernet Cables** | Belden Cat6 UTP Cable (305m box) | 2 | High-speed gigabit copper cabling running through conduit to all desktop faceplates and WAPs[cite: 1]. |
| **RJ45 Connectors & Boots** | Pass-Through Cat6 RJ45 | 200 | Connectors for terminating patch cables and wall drops[cite: 1]. |

---

## PART 5: Enterprise Network Diagram[cite: 1]

![Enterprise Network Topology](diagrams/NetworkTopology.png)

### Topological Hierarchy & Connections
1. **Edge Infrastructure:** `Internet` → `ISP Fiber Modem` → `pfSense Hardware Firewall` → `MikroTik Core Router`[cite: 1].
2. **Distribution Tier:** The `MikroTik Core Router` connects directly via trunk link to the `Cisco 48-Port Managed Switch`[cite: 1].
3. **Core Server Services:** Connected directly to dedicated Switch Ports (VLAN 10 - Servers):
   * Ubuntu Dell PowerEdge Server[cite: 1]
   * Synology 4-Bay NAS Storage[cite: 1]
   * Central Network Laser Printer[cite: 1]
4. **Wireless Infrastructure:** Connected via PoE switch ports:
   * 2x Ubiquiti Access Points (Serving Sales Laptops & Isolated Guest Network)[cite: 1].
5. **VLAN Segmentation Architecture:**
   * **VLAN 10 (Management & Servers):** `192.168.10.0/24` → Ubuntu Server, NAS, Printer, Core Switch, WAPs[cite: 1].
   * **VLAN 20 (IT Dept):** `192.168.20.0/24` → 5x Workstation Desktops[cite: 1].
   * **VLAN 30 (HR Dept):** `192.168.30.0/24` → 4x Workstation Desktops[cite: 1].
   * **VLAN 40 (Finance Dept):** `192.168.40.0/24` → 5x Workstation Desktops[cite: 1].
   * **VLAN 50 (Sales Dept):** `192.168.50.0/24` → 6x Laptops via Wi-Fi/Ethernet drops[cite: 1].

---

## PART 6: System Administration Roles[cite: 1]

### 1. Helpdesk Technician[cite: 1]
* **Core Responsibilities:** Serves as the Tier-1 line of support for end-user issues[cite: 1]. Installs OS images, configures user workstations, troubleshoots hardware/peripheral failures, manages password resets, and logs incidents in the ticketing system.
* **Key Skills:** OS troubleshooting (Windows/macOS), basic networking diagnostics, customer service, hardware assembly, active listening.
* **Common Tools:** Jira Service Desk, Freshdesk, AnyDesk, Sysinternals Suite, Windows Active Directory Users & Computers.
* **Certifications:** CompTIA A+, Microsoft Certified: Modern Desktop Administrator Associate, ITIL Foundation.

### 2. Network Administrator[cite: 1]
* **Core Responsibilities:** Oversees physical and logical network infrastructure[cite: 1]. Configures switch VLANs, router tables, firewall filtering rules, wireless networks, and monitors network performance/uptime to prevent bottlenecks or unauthorized intrusions.
* **Key Skills:** IP subnetting, VLAN configuration, routing protocols (OSPF, BGP), firewall policy rulesets, packet analysis, structured cabling.
* **Common Tools:** Wireshark, Cisco Packet Tracer, PuTTY, SolarWinds Network Performance Monitor, PRTG.
* **Certifications:** Cisco Certified Network Associate (CCNA), CompTIA Network+, Juniper JNCIA.

### 3. Linux System Administrator[cite: 1]
* **Core Responsibilities:** Manages enterprise Linux servers[cite: 1]. Handles installation, kernel updates, security hardening, user access management, shell scripting automation, and maintaining system service health (Web servers, databases, DNS, SSH).
* **Key Skills:** Bash/Python scripting, Linux CLI, systemd, user/permission management (POSIX/ACLs), package management (apt/yum), RAID/LVM configuration.
* **Common Tools:** Bash, Ansible, SSH, htop, Webmin, Docker, Nginx/Apache.
* **Certifications:** Red Hat Certified System Administrator (RHCSA), Linux Professional Institute LPIC-1, CompTIA Linux+.

### 4. Cloud Administrator[cite: 1]
* **Core Responsibilities:** Provisions and maintains cloud infrastructure environments[cite: 1]. Monitors cloud expenditures, manages Identity and Access Management (IAM) policies, configures virtual networks (VPCs), and handles automated cloud backups and disaster recovery.
* **Key Skills:** Cloud architecture design, IAM security, Infrastructure as Code (IaC), cost optimization, cloud storage management.
* **Common Tools:** AWS Management Console, Azure Portal, Terraform, AWS CLI, CloudWatch.
* **Certifications:** AWS Certified SysOps Administrator, Microsoft Certified: Azure Administrator Associate.

### Inter-Role Collaboration in the Organization[cite: 1]
These four specialists function as an integrated technical unit[cite: 1]. When a user reports poor application response times, the **Helpdesk Technician** logs and isolates the issue at the workstation level before escalating network-related anomalies to the **Network Administrator**[cite: 1]. The Network Admin verifies VLAN traffic and routing health across switches[cite: 1]. If traffic flow is optimal, the **Linux Administrator** inspects application logs, database queries, and CPU utilization on the local servers[cite: 1]. Meanwhile, the **Cloud Administrator** coordinates with the Linux Admin to scale resources seamlessly into cloud environments or offsite backups[cite: 1]. This creates a smooth operational pipeline from end-user endpoints to core server infrastructures[cite: 1].

---

## PART 7: Infrastructure Recommendations[cite: 1]

### Internet Provider Selection
* **Primary Recommendation:** PLDT Enterprise Fiber (300 Mbps Symmetric Dedicated Line with Static IP).
* **Secondary / Redundancy:** Converge ICT Business Fiber (100 Mbps Backup Line).
* **Justification:** A symmetric dedicated line guarantees equal upload and download speeds, which is crucial for software developers pushing large code repositories and docker builds. Dual-ISP routing on the MikroTik router ensures automatic failover so business operations remain online if one ISP experiences an outage.

### Server Specifications
* **Hardware:** Dell PowerEdge R450 Rack Server.
* **Specs:** Intel Xeon Silver 4310 processor, 64GB DDR4 ECC RAM, Dual 2TB Enterprise SAS HDDs running hardware RAID 1 (Mirrored).
* **Justification:** ECC memory prevents silent data corruption. RAID 1 provides disk fault tolerance—if one drive fails, the server continues operating without data loss while the bad drive is replaced.

### Backup Strategy (3-2-1 Compliance)
* **3 Copies of Data:** Primary server storage, local NAS storage, and offsite cloud storage.
* **2 Different Media Types:** Synology NAS (Local Network Disk) and External Hard Drives / Cloud.
* **1 Offsite Location:** Encrypted cloud backup (AWS S3 Glacier) combined with weekly physical offline drive rotations stored in a secure offsite location.

### Endpoint & Network Security
* **Antivirus / Endpoint Security:** Deploy **Microsoft Defender for Business** across all desktop and laptop endpoints. Centrally managed via cloud dashboard to enforce automatic daily virus definition updates and real-time threat scanning.
* **Password Policy:** Enforce a strict Domain Group Policy (GPO):
  * Minimum length: 12 characters.
  * Complexity: Requires uppercase, lowercase, numbers, and symbols.
  * Expiration & History: Passwords expire every 90 days; prevents re-use of the last 5 passwords.
  * Multi-Factor Authentication (MFA): Mandatory across all Microsoft 365, VPN, and GitHub accounts.
  * Lockout Policy: Account locks out after 5 consecutive failed attempts.

### Infrastructure Expansion Plan
* **Network Scalability:** The selected Cisco 48-port switch provides 20+ unused ports, easily accommodating 100% headcount expansion without requiring new core networking hardware.
* **Subnetting Capacity:** All departmental VLANs use `/24` subnets (supporting up to 254 hosts each), allowing each department to expand significantly within its allocated IP space.

---

## PART 8: Personal Reflection[cite: 1]

Completing this Enterprise Infrastructure Planning project provided valuable practical perspective on system administration concepts beyond theoretical learning[cite: 1]. I gained a clearer understanding of how business requirements directly dictate technical hardware purchasing, network segmentation, and security choices[cite: 1]. Designing an entire infrastructure from scratch highlighted that system administration is as much about risk management, budgeting, and organization as it is about configuring command-line interfaces[cite: 1].

The most challenging task was designing the enterprise network topology and structuring the VLAN segmentation model[cite: 1]. Balancing logical isolation between departments—such as ensuring Finance data remains separated from general Wi-Fi traffic—while maintaining necessary shared access to printers and primary server resources required careful mapping on Draw.io[cite: 1]. Correctly aligning subnet spaces with physical switch port assignments demanded attention to detail[cite: 1].

This project underscored why thorough planning must precede physical deployment[cite: 1]. Purchasing hardware or installing software without a clear blueprint leads to network bottlenecks, IP address conflicts, security vulnerabilities, and wasted financial resources[cite: 1]. A well-documented infrastructure plan acts as a clear roadmap, reducing downtime and simplifying future troubleshooting[cite: 1]. 

Ultimately, this portfolio project helped build my confidence as an aspiring System Administrator[cite: 1]. It strengthened my technical documentation skills in Markdown, my network design capabilities, and my ability to justify technical decisions from a business standpoint[cite: 1].

---

## References[cite: 1]
1. Cisco Systems. (2023). *Cisco Catalyst 2960-X Series Switches Data Sheet*.
2. Dell Technologies. (2023). *Dell PowerEdge R450 Spec Sheet*.
3. MikroTik. (2024). *RouterBOARD RB4011iGS+RM User Manual*.
4. Netgate. (2024). *pfSense Plus Security Gateway Documentation*.
