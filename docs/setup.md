# Setup Overview

## Virtual Machine Environment
Two virtual machines were deployed using Oracle VirtualBox:

- Ubuntu Linux running the Wazuh Manager, Indexer, and Dashboard
- Windows 11 Pro running the Wazuh Agent

Both VMs use the **Bridged Adapter** networking mode, allowing them to communicate directly over the same local network.

---

## Wazuh Manager Setup
The Wazuh Manager, Indexer, and Dashboard were installed on the Ubuntu VM.  
Once running, the dashboard was accessed through a web browser using the Ubuntu VM's local IP.

---

## Wazuh Agent Setup
The Windows 11 VM was configured with the Wazuh Agent.  
During installation, the manager’s IP address was entered so the agent could communicate back to the server.  
The agent service was started and verified through the Wazuh Dashboard.

---

## Monitoring Configuration
A specific folder on the Windows system was selected as the monitored directory.  
File creation, modification, and deletion were tested, and corresponding alerts appeared on the dashboard.

---

## Verification Steps
To ensure the lab was functioning correctly:

1. The Windows agent’s connection status was confirmed.  
2. Folder activity was performed to trigger FIM events.  
3. Alerts were reviewed in the Wazuh Dashboard.  
4. Event details were inspected for context such as file path and timestamp.

---

## Summary
The setup successfully demonstrated real-time file integrity monitoring and secure communication between the Wazuh Manager and Agent.
