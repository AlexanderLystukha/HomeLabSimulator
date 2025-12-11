# HomeLab Simulator

## Overview
This home lab simulator demonstrates how an actual home lab would function within a network topology. I created this project to gain hands-on experience with network configuration and security implementation, preparing myself for setting up real-world home labs and enterprise networks.

The simulator focuses on practical networking concepts including network segmentation, access control, VPN configuration, and security isolation—all essential skills for modern network administration and cybersecurity.

## Project Goals
- Gain experience in home lab network architecture and security
- Practice network segmentation and VLAN configuration
- Implement access control lists (ACLs) for traffic management
- Configure secure remote access via VPN
- Simulate threat monitoring using honeypot isolation

---

## Key Features

### 1. Home Network Architecture
The home network implements multiple security layers and network segmentation:

- **Wireless Security**: WPA2-Personal encryption for wireless connections (smartphones, laptops)
- **Network Segmentation**: Isolated server network for enhanced security
- **VLAN Configuration**: Two VLANs within the server network
  - Server VLAN: Houses critical infrastructure
  - Honeypot VLAN: Isolated threat monitoring environment
- **Access Control Lists (ACLs)**: Layer 3 traffic filtering between networks
  - Inbound ACL for external traffic
  - Inbound ACL for server network protection
  - Outbound ACL for honeypot traffic restriction

<img width="944" height="484" alt="Home Network Topology" src="https://github.com/user-attachments/assets/9ca4a5e1-41da-40b6-8121-6eef5d5c22fc" />

---

### 2. Remote Access VPN
Secure remote connectivity using industry-standard protocols:

- **IPsec Architecture**: Encrypted and authenticated connections between VPN clients and the network
- **ISAKMP Protocol**: Secure key exchange and connection establishment (part of IPsec suite)
- **Restricted Access**: VPN users can only access:
  - Network Attached Storage (NAS)
  - Proxmox server

<img width="411" height="309" alt="VPN Configuration" src="https://github.com/user-attachments/assets/e7ff704b-d3c7-4c3c-aed0-cea6eab3d865" />

---

### 3. Honeypot Isolation
A dedicated threat monitoring system completely isolated from production resources:

- **Complete Isolation**: Honeypot is fully separated from the home network and server infrastructure
- **Open Access**: External traffic is allowed to reach the honeypot for threat research
- **Strict ACL Rules**: 
  - Blocks all outbound traffic from honeypot to servers and home devices
  - Main control center maintains monitoring access for threat analysis

<img width="509" height="159" alt="Honeypot Isolation" src="https://github.com/user-attachments/assets/c93cd3e2-7f23-40bc-a3e8-31a6527ddb9a" />

---

### 4. Enterprise Wireless Security
A separate wireless network demonstrating enterprise-grade security:

- **WPA2-Enterprise**: Implements RADIUS-based authentication
- **Purpose**: Simulates secure corporate wireless infrastructure
- **Use Case**: Demonstrates the difference between personal and enterprise wireless security models

<img width="290" height="227" alt="Enterprise Wireless Network" src="https://github.com/user-attachments/assets/f8ca8f2e-162b-40ae-8714-3d933281fb4f" />

---

## Technologies Used
- **Cisco Packet Tracer**: Network simulation and design
- **IPsec/ISAKMP**: VPN security protocols
- **WPA2-Personal/Enterprise**: Wireless security standards
- **VLANs**: Network segmentation
- **ACLs**: Traffic filtering and security policies

## Getting Started
1. Download and install the latest [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer)
2. Clone this repository or download the file directly from this repository
3. Open the `.pkt` file in Packet Tracer
4. Explore the network topology and configuration

## Skills Demonstrated
- Network topology design
- VLAN configuration and management
- Access control list implementation
- VPN setup and configuration
- Security best practices (network segmentation, honeypot deployment)
- Wireless network security (WPA2-Personal and Enterprise)
