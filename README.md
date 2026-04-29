## Overview

This project simulates an enterprise network with:

* 1 Headquarters (HQ)
* 2 Branch offices
* Redundant LAN design at HQ
* Secure WAN connectivity using DMVPN + IPsec

---

## Technologies Used

### LAN (HQ)

* OSPF for inter-VLAN routing
* HSRP for gateway redundancy
* VLAN segmentation:

  * VLAN 10 – Accounting & Finance
  * VLAN 20 – Sales & BD
  * VLAN 30 – Executive & Management
  * VLAN 40 – IT
  * VLAN 50 – Servers
  * VLAN 60 – DMZ

### WAN

* DMVPN (Hub-and-Spoke)
* IPsec for encryption
* EIGRP for dynamic routing over DMVPN

---

## Network Design

* HQ acts as DMVPN Hub
* Branch1 and Branch2 are Spokes
* Dual distribution switches at HQ with HSRP
* OSPF used internally at HQ
* EIGRP used across WAN (DMVPN tunnel)

---

## Security

* IPsec applied over DMVPN tunnels
* DMZ segment for public-facing servers

---


##  Network Topology

![DMVPN Topology](https://github.com/abdelrahman0x01/Multi-Site-Enterprise-Network-with-DMVPN/blob/main/topology/Network-topology.png?raw=true)

---
## Verification

* Inter-VLAN connectivity ✔
* Branch-to-branch communication ✔
* HSRP failover ✔
* DMVPN tunnel stability ✔
* Encrypted traffic over WAN ✔
![Verifyication_hq_to_b1](https://github.com/abdelrahman0x01/Multi-Site-Enterprise-Network-with-DMVPN/blob/main/Verification/HQ%20to%20B1.png?raw=true)
![Verifyication_hq_to_b2](https://github.com/abdelrahman0x01/Multi-Site-Enterprise-Network-with-DMVPN/blob/main/Verification/HQ%20to%20B2.png?raw=true)

---

## How to Use

1. Import configs into your lab (EVE-NG)
2. Apply configurations per device
3. Verify using provided test cases

   ---
*Note* Password:Cisco

