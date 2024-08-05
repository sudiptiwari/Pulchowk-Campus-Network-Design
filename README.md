# Project Report On Design of Pulchowk Campus Autonomous System in Cisco Packet Tracer

### TRIBHUVAN UNIVERSITY
### INSTITUTE OF ENGINEERING
### PULCHOWK CAMPUS

**Submitted By:**  
Name: Sudip Tiwari  
Roll No: 077BCT085  
Group: D  

**Submitted To:**  
Department of Electronics and Computer Engineering  

## Introduction
**Project Overview:**  
This proposal consists of a network design effort that attempts to envisage the Network Topology and functioning of Pulchowk Campus, IoE. The proposal ventures on realizing the Campus Network as an Autonomous System with an effort to model the campus network architecture as accurately as possible. This project implements concepts from Computer Networks and Security theory and practical classes.

**Objectives:**  
The primary objective of this project is to design and implement a functional network topology for Pulchowk Campus, IoE, using Cisco Packet Tracer. The design divides the campus network into four OSPF areas, each representing different segments of the campus network, to achieve efficient data communication and connectivity across various departments and facilities within the campus.

## Network Design
**Topology Overview:**  
The network design for Pulchowk Campus, IoE, is divided into four OSPF areas to represent different segments of the campus network. Each area is color-coded in the network diagram for easy identification and management.

- **Area 0 (Blue):** Contains the CIT ASBR and CIT Library Subnet, including a web server for "pulchowk.com". This area also includes two VLANs, namely ICTC & DoECE Students and ICTC & DoECE Faculty, along with a DNS Server.
- **Area 1 (Brown):** Encompasses the Whitehouse and Architecture Subnets, along with the Web Server for "ioe.com".
- **Area 2 (Pink):** Comprises the Mechanical Department Router, which is further divided into two VLANs for Mechanical and Aerospace Department LANs. This area also includes the Civil Department Router and the Applied Science Router, where the second DNS Server is connected.
- **Area 3 (Green):** Includes the Hostel zone, consisting of a Boys Hostel Router with three VLANs dividing the network into Block A, Block B, and Block C VLANs. This area also includes a Girls Hostel Router.

### IP Addresses
The following pool of IP Addresses of two networks were acquired:
- 24.24.24.0/21
- 24.24.32.0/21

The division of IP Addresses for each subnet using VLSM resulted into:

| S.N | Department | No. of IPs Required | Subnet Mask | Net-ID | Usable IP Range | Broadcast Address |
|-----|------------|---------------------|-------------|--------|-----------------|-------------------|
| 1 | ICTC | 550 | 255.255.252.0 | 24.24.24.0 | 24.24.24.1 - 24.24.26.254 | 24.24.27.255 |
| 2 | DoECE | 300 | 255.255.254.0 | 24.24.28.0 | 24.24.28.1 - 24.24.29.254 | 24.24.29.255 |
| ... | ... | ... | ... | ... | ... | ... |

### IP Address of each Server
- **Web Server for “pulchowk.com”**: 24.24.35.227
- **Web Server for “ioe.com”**: 24.24.34.126
- **DNS 1**: 24.24.29.254
- **DNS 2**: 24.24.35.190
- **Root DNS at ISP**: 20.20.20.6

## Implementation
**Devices and Connections:**  
- **Routers**: Router-PT
- **Switches**: Switch 2960-24 TT
- **Servers**: DNS servers and Web servers for specific subnets

The network design includes VLAN configurations on three different switches to segregate traffic and improve network management. Configuration details include setting up OSPF areas, configuring IP addresses and subnet masks per the VLSM scheme, creating and managing VLANs, and configuring DNS and Web servers.

## Testing and Results
- **Ping Test**: All PCs successfully pinged any other PC in the network.
- **Web Server Access Test**: All PCs were able to browse the web servers "pulchowk.com" and "ioe.com" without any issues.

## Conclusion
The network design for Pulchowk Campus, IoE, was successfully implemented using Cisco Packet Tracer, meeting all the objectives and ensuring optimal network functionality and connectivity.
