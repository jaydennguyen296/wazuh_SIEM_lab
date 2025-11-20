# wazuh_SIEM_lab
This project sets up a free, lightweight SIEM lab using Wazuh. The goal is to build a practical training environment for security monitoring, log analysis, and SOC-analyst style investigations — all using open-source tools.

## Overview
This repository documents my ongoing work with Wazuh, focusing on endpoint monitoring and detection using a virtualized homelab environment.  
The first completed component of this project is **File Integrity Monitoring (FIM)** on a Windows 11 system, with events collected and analyzed by a Wazuh Manager hosted on Ubuntu.

This project will continue to expand as I add more monitoring modules, rules, integrations, and cybersecurity scenarios.

---

## Current Scope: Windows File Integrity Monitoring
The initial phase of the project demonstrates real-time monitoring of a Windows folder.  
The setup includes:

- A Wazuh Manager running on Ubuntu  
- A Wazuh Agent installed on Windows 11 Pro  
- Both systems are virtual machines running in VirtualBox  
- Networking is configured using the Bridged Adapter mode  
- A Windows folder is monitored for file creation, modification, and deletion  

The Wazuh Dashboard successfully displays alerts when activity occurs in the monitored folder.

---

## Technologies Used
- Wazuh Manager (Ubuntu Linux)  
- Wazuh Agent (Windows 11 Pro)  
- VirtualBox virtualization  
- Bridged networking  
- Wazuh File Integrity Monitoring (FIM)  
- Wazuh Dashboard for event review  

---

## Current Features
- Real-time detection of file creation  
- Real-time detection of file modification  
- Real-time detection of file deletion  
- Event forwarding from Windows agent to Wazuh Manager  
- Centralized viewing of alerts through the Wazuh Dashboard  

These results confirm that agent-to-manager communication is healthy and that FIM is functioning as expected.

---

## Project Goals  
This repository will eventually include multiple components of endpoint and network security monitoring.  
Planned areas of development include:

### Endpoint Monitoring Expansion
- Additional folders and sensitive paths added to FIM  
- Windows registry monitoring  
- Process and service monitoring  
- Sysmon integration  
- Custom Wazuh rules for detecting suspicious behavior  

### Network & Infrastructure Monitoring
- Linux endpoint monitoring  
- Web server monitoring  
- Log collection from multiple systems  
- Alert correlation across endpoints  

### Detection Engineering
- Creating custom detection rules  
- Generating alerts for malware-like behavior  
- Testing detections using realistic attack simulation  
- Building dashboards for SOC-style investigation  

### Integrations & Automation
- SIEM integration (Elastic, Splunk, or Graylog)  
- Alerting via email, Slack, or Teams  
- Automated response scenarios  
- Threat hunting scripts  

---

## Why This Project Exists
This lab is part of my ongoing learning journey in cybersecurity and detection engineering.  
It allows me to:

- Explore real-world security monitoring concepts  
- Build practical, hands-on skills  
- Understand how endpoint activity is collected, analyzed, and responded to  
- Create a foundation for advanced SOC/homelab projects  
- Document progress for others to learn from

---

## Status  
This project is active and evolving.  
More features, modules, and documentation will be added over time.  
The current version represents only the **first stage** of a much larger lab environment.

---

## Future Updates  
Upcoming additions may include:

- Additional operating systems  
- Server monitoring  
- MITRE ATT&CK–aligned detections  
- Better documentation and diagrams  
- A full SOC-style lab with multiple systems  

---


## Acknowledgments
Thanks to Wazuh for its powerful open-source security platform and documentation.