# Architecture

## Overview
This document describes the architecture of the Wazuh Endpoint Monitoring Lab.  
The environment consists of two virtual machines operating in the same bridged network and communicating directly without NAT limitations.

---

## Components

### 1. Wazuh Manager (Ubuntu)
- Hosts the Wazuh Manager, Indexer, and Dashboard  
- Processes logs and generates alerts  
- Provides the web interface for analysis

### 2. Windows 11 Pro (Wazuh Agent)
- Runs the Wazuh Agent service  
- Monitors selected directories for file creation, modification, and deletion  
- Sends events to the Wazuh Manager

### 3. VirtualBox Hypervisor
- Used to virtualize both systems  
- Networking configured in **Bridged Adapter** mode  
- Allows both VMs to receive IPs from the local network and communicate like physical hosts

---

## Communication Flow

1. The Windows Agent monitors the specified folder.  
2. When file activity occurs, the agent logs the event.  
3. The agent forwards the event to the Wazuh Manager over the bridged network.  
4. The Manager processes the event, enriches it, and stores it in the indexer.  
5. The event becomes visible on the Wazuh Dashboard for analysis.

---

## Diagram Description (Text)

    [Windows 11 VM] --(Agent Logs)--> [Wazuh Manager VM] --(Processed Events)--> [Wazuh Dashboard]

    Both virtual machines operate on the same LAN thanks to bridged networking.

---

## Summary
This architecture mirrors a simplified real-world SOC monitoring environment, with centralized log collection and agent-based monitoring on endpoints.
