# Enterprise Hybrid Network Infrastructure & Secure WAN Interconnectivity

## Project Overview
This project demonstrates the design, implementation, and optimization of a scalable enterprise network architecture, connecting a Headquarters (HQ) site with a Branch office. The solution integrates core switching technologies, advanced redundancy protocols, and secure wide-area network (WAN) connectivity to ensure high availability, efficient traffic management, and robust data protection.

---

## Key Technical Pillars

*   **Core Network Foundation:** The network utilizes a resilient core layer featuring L3 EtherChannel for high-bandwidth uplinks between core switches. VLAN segmentation, driven by a centralized VTP domain, ensures logical isolation and efficient broadcast control.
*   **High Availability & Load Balancing:** To eliminate single points of failure, the architecture leverages VRRP (Virtual Router Redundancy Protocol) in an Active/Active configuration. This design effectively distributes inter-VLAN routing traffic between core switches, optimizing resource utilization and guaranteeing rapid failover.
*   **Secure WAN Architecture:** Connectivity between the HQ and the Branch is secured through a robust GRE over IPsec tunnel. This implementation ensures that inter-site traffic remains confidential and tamper-proof while traversing public ISP infrastructure.
*   **Dynamic Routing & Internet Egress:** OSPF is deployed throughout the topology to ensure dynamic path discovery and convergence. Internet connectivity is managed via NAT (Network Address Translation) at the HQ gateway, providing secure access for internal services while shielding the private addressing scheme.
*   **Service Delivery & Security:** The project features a multi-service server environment within a secure zone, protected by granular Access Control Lists (ACLs) that restrict unauthorized access while allowing designated traffic to enterprise applications.

---

## Infrastructure Scope
The environment simulates a real-world enterprise scenario comprising:

*   **Core Layer:** Redundant L3 switches providing the backbone routing and gateway redundancy.
*   **Access Layer:** Managed switches supporting departmental VLAN segmentation (IT, Management, Sales, Finance, HR).
*   **Edge/WAN Layer:** Integrated routing for secure site-to-site communication, utilizing public addressing for WAN links and private subnets for internal host management.

---

## Network Architectural Zones

*   **HQ LAN Zone:** Comprises the Core Layer (L3 EtherChannel switches) and the Access Layer (VLANs for IT, Management, Sales, Finance, and HR).
*   **HQ Server Zone:** A dedicated segment hosting enterprise applications (Web, File, Logs) protected by ACLs.
*   **WAN Transit Zone:** Point-to-Point public links (/30) connecting HQ and Branch routers via an ISP transit network.
*   **Secure Tunnel Zone:** GRE over IPsec overlay facilitating encrypted site-to-site communication between HQ and Branch.
*   **Branch LAN Zone:** Distribution and Access switches implementing departmental VLANs (HR, Sales, Management) with Router-on-a-Stick inter-VLAN routing.
*   **Management & Routing Zone:** Loopback interfaces for stable router identity and OSPF for dynamic inter-site path convergence.

---
## Directory Structure
- `Documentation_ccna-project/`: Project reports and design requirements.
- `images/`: Network topology screenshots and validation evidence.
- `manual_config/`: CLI configuration scripts for Cisco routers and switches.
- `pnetlab_config/`: Exported configurations from the PNETLab simulation.

---

## Connect With Me
www.linkedin.com/in/abdelrhman-mosaad

*View full project documentation on https://canva.link/xgy5x0dv7p7rs2e*
