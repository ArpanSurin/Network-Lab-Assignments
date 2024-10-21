# Lab Exam Exercise: Network Topology using RIP and OSPF

## Project Overview
This project demonstrates the configuration of a network topology using RIP v1 and OSPF routing protocols in Cisco Packet Tracer.\
The objective of the lab was to design two Local Area Networks (LANs) connected by routers, each using a different routing protocol, and to ensure communication between the LANs through proper routing. The network design was simulated and tested in Cisco Packet Tracer to verify connectivity.

## Topology Details
The network consists of :

 **LAN 1 :**
- 5 PCs connected to Switch 1
- Router 1 connected to Switch 1, configured with RIP v1.

**LAN 2 :**
- 5 PCs connected to Switch 2
- Router 2 connected to Switch 2, configured with OSPF
WAN: A serial connection between Router 1 and Router 2 for inter-router communication.

## IP Address Configuration

**LAN 1 :** `192.168.1.0/24`
- **PCs :** `192.168.1.xxx` (where xxx is the last three digits of the roll number)
- **Router 1 LAN interface :** `192.168.1.1`

**LAN 2 :** `192.168.2.0/24`
- **PCs :** `192.168.2.xxx`
- **Router 2 LAN interface :** `192.168.2.1`

**WAN:** `192.168.10.0/30`
- **Router 1 WAN interface :** `192.168.10.1`
- **Router 2 WAN interface :** `192.168.10.2`

## Routing Protocols Configuration
**Router 1 :** Configured with RIP v1
- **Networks :** `192.168.1.0`, `192.168.10.0`

**Router 2 :** Configured with OSPF
- **Networks :** `192.168.2.0`, `192.168.10.0`

## Simulation and Testing
The network was tested using ping and traceroute commands to verify connectivity between devices in LAN 1 and LAN 2. Cisco Packet Tracer's simulation mode was used to trace the packet routes between the two LANs.

## Files in the Repository
- **Lab_Exam_Report.docx:** A detailed report of the project including network design, IP configuration, and routing protocols.
- **Screenshots:** Images capturing the network topology and successful message transmission.
- **Exercise_2.pkt:** The Packet Tracer file containing the configured network.

## How to Run
1. Open the Exercise_2.pkt file in Cisco Packet Tracer.
2. Explore the network topology, check device IP configurations, and inspect the routing table on both routers.
3. Use simulation mode in Cisco Packet Tracer to test message transmission across the network.

## Conclusion
This lab successfully demonstrates how to configure a network with multiple routing protocols (RIP v1 and OSPF) and ensure proper packet routing between two separate LANs. The configuration was verified through successful message transmission in Cisco Packet Tracer.