# Hotel Network Management

A three-floor hotel network designed and implemented in Cisco Packet Tracer.

## Overview
The network connects eight departments across three floors. Each department has its own VLAN and subnet. Three routers are linked with serial connections, OSPF is used for routing, and DHCP assigns addresses automatically.

## Topology
![Topology](screenshots/01-topology.png)

## Departments and VLANs
| Floor | Department | VLAN | Network |
|---|---|---|---|
| 1st | Reception | 80 | 192.168.8.0/24 |
| 1st | Store | 70 | 192.168.7.0/24 |
| 1st | Logistics | 60 | 192.168.6.0/24 |
| 2nd | Finance | 50 | 192.168.5.0/24 |
| 2nd | HR | 40 | 192.168.4.0/24 |
| 2nd | Sales | 30 | 192.168.3.0/24 |
| 3rd | Admin | 20 | 192.168.2.0/24 |
| 3rd | IT | 10 | 192.168.1.0/24 |

## Router Links
| Link | Network |
|---|---|
| F3 - F2 | 10.10.10.0/30 |
| F3 - F1 | 10.10.10.4/30 |
| F2 - F1 | 10.10.10.8/30 |

## Features Implemented
- VLANs and 802.1Q trunking
- Inter-VLAN routing (router-on-a-stick)
- OSPF (Area 0)
- DHCP on each router
- SSH for remote access
- Port security (sticky MAC, shutdown mode) on the IT switch

## Screenshots
- OSPF neighbors: ![OSPF](screenshots/02-ospf-neighbors.png)
- Connectivity test: ![Ping](screenshots/09-ping.png)
- Port security: ![Port Security](screenshots/11-port-security.png)

## Files
- `HotelNetwork.pkt`: Packet Tracer project file
- `configs/`: running configuration of every device

## Tools
Cisco Packet Tracer, Cisco IOS CLI

## Author
Muhammad Abbas