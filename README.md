# Cybersecurity Homelab Project

## Objective
The Cybersecurity Homelab project was designed to create a simulated business network within a virtualized environment using VMware Workstation.  
This project’s main goal was to **implement, configure, and connect multiple systems** to replicate a real-world enterprise infrastructure — allowing for practical experience with **networking, security tools, and system administration**.  

Through this homelab, I gained hands-on experience setting up and managing Windows and Linux servers, a firewall, a SIEM solution, and a vulnerability scanner to detect and analyze potential security issues within the environment.

---

### Skills Learned

- Configuration and management of **Active Directory Domain Services (AD DS)**  
- Setup and maintenance of **Windows Server** and **Linux servers**  
- Implementation of **network segmentation** and **firewall rules**  
- Integration and usage of **SIEM tools** for centralized log collection and analysis  
- Deployment and operation of **vulnerability scanners** (e.g., OpenVAS)  
- Configuration of **VPN** for secure remote connections  
- Understanding of **email server configurations** and internal communications  
- Practical knowledge of **incident detection**, **response**, and **system hardening**  

---

### Tools Used

- **Virtualization Software:** VMware Workstation  
- **Operating Systems:** Windows Server 2019, Windows 10, Ubuntu Server  
- **Firewall:** pfSense  
- **Vulnerability Scanner:** OpenVAS  
- **SIEM:** Wazuh (or Splunk / ELK Stack)  
- **VPN:** OpenVPN  
- **Email Server:** Postfix / Mailcow (optional setup)  
- **Network Analysis Tools:** Wireshark, tcpdump  
- **Monitoring and Logging:** Syslog, Event Viewer  

---

## Steps

<img width="1918" height="1010" alt="image" src="https://github.com/user-attachments/assets/6f6da402-e257-4b5e-b465-4a7803ef8115" />
These are the lists of my VM.
<img width="594" height="523" alt="image" src="https://github.com/user-attachments/assets/98c473de-d60f-4705-8963-6ec43a3f11cf" />
This is my Network names for my VM.

> 💡 Every screenshot should have a short caption and explanation of what’s being shown.

---

**Ref 1: Network Topology Diagram**  
![Network Diagram](network-diagram.png)

**Explanation:**  
This diagram represents the virtual network layout of the homelab environment.  
The network is segmented into zones:  
- Internal LAN (AD Domain, Workstations)  
- DMZ (Web Server, Email Server)  
- Security Segment (SIEM, Vulnerability Scanner)  
All traffic is filtered through the **pfSense firewall**, with logs forwarded to the **SIEM** for monitoring.

---

**Ref 2: VMware Virtual Machines**  
![VMware Setup](screenshots/vmware-setup.png)

**Explanation:**  
Each VM was configured with separate network adapters to simulate LAN, WAN, and management networks.  
Snapshots were taken after key configuration steps to maintain restore points.

---

**Ref 3: Active Directory Setup**  
![Active Directory Setup](screenshots/ad-setup.png)

**Explanation:**  
Windows Server was configured as a Domain Controller with AD DS installed.  
User accounts, Organizational Units (OUs), and Group Policies were created to simulate an enterprise environment.

---

**Ref 4: Firewall Configuration (pfSense)**  
![pfSense Dashboard](screenshots/pfsense-dashboard.png)

**Explanation:**  
pfSense was used to manage traffic between internal networks and the simulated internet.  
Custom firewall rules were added to restrict certain ports, and NAT was configured for outbound connections.

---

**Ref 5: SIEM Deployment**  
![SIEM Dashboard](screenshots/siem-dashboard.png)

**Explanation:**  
The Wazuh server was deployed on Ubuntu and configured to collect logs from Windows and Linux hosts.  
This central monitoring allowed for real-time detection of suspicious activity and system alerts.

---

**Ref 6: Vulnerability Scanning (OpenVAS)**  
![OpenVAS Scan Results](screenshots/openvas-scan.png)

**Explanation:**  
OpenVAS was used to perform network vulnerability scans against all connected hosts.  
Results were analyzed and correlated with SIEM data to verify detection and response capabilities.

---

## Results / Findings
- Successfully created a virtualized enterprise-style network using VMware Workstation.  
- Detected simulated attacks and unusual login attempts through SIEM alerts.  
- Configured multiple security layers — firewall, VPN, and patch management.  
- Scanned systems for vulnerabilities and implemented remediation steps.  
- Improved understanding of how enterprise systems communicate and defend against threats.

---

## Future Improvements
- Integrate **Intrusion Detection / Prevention Systems** (Snort or Suricata).  
- Automate VM deployment using **Ansible** or **PowerShell scripts**.  
- Expand homelab to include **web application servers** for web security testing.  
- Implement **phishing simulation** using a self-hosted mail server.  
- Add **Elastic Stack (ELK)** for deeper log analysis and visualization.

