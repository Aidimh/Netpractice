# Netpractice
A networking and infrastructure project from the 42 Network (1337) curriculum focused on routing, subnetting, and network troubleshooting. Solved complex configuration puzzles by calculating IPv4 masks, defining subnet boundaries, managing routing tables, and structuring gateway connections for reliable packet transmission.
# NetPractice — Networking, Subnetting & Routing Architecture

An intensive infrastructure project from the **1337 / 42 Network** curriculum designed to master the fundamentals of the **TCP/IP networking model**. The core objective of this project is to troubleshoot and configure broken networks by modifying IP addresses, subnets, masks, and routing tables to establish flawless packet delivery.

This project bridges the gap between software development and low-level system operations, laying the groundwork for complex infrastructure projects like **Inception**.

---

## 🛠️ Key Architectural & Networking Concepts Mastered

* **IPv4 Address Structuring:** Analyzing and breaking down 32-bit IPv4 addresses to manage network portions, host portions, and broad broadcast boundaries.
* **Subnetting & Variable Length Subnet Masking (VLSM):** Crafting precision subnet strategies using CIDR notation (e.g., `/24`, `/28`, `/30`) to isolate network segments while optimizing IP address conservation.
* **Routing Table Optimization:** Engineering accurate static routing entries containing explicit Destination IPs, Gateways (`next-hop`), and Network Interfaces to chart the shortest path for network packets.
* **Network Entity Topologies:** Configuring the behavioral properties of essential infrastructure nodes:
  * **Client Devices / Internet Hosts:** Endpoints requiring an IP, a subnet mask, and a default gateway to escape local subnets.
  * **Switches:** Local area Layer-2 link layers passing untagged packets within the identical broadcast domains.
  * **Routers:** Layer-3 gateway units executing packet sorting and cross-network routing modifications between completely separate subnets.
* **NAT & Private IP Space:** Managing address translations and working across standard internal private networks (`10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16`).

---

## 📋 Sample Networking Matrix Reference

To solve the configuration scenarios, the following binary arithmetic conversions were utilized to map host ranges and eliminate IP conflicts:


| CIDR Prefix | Subnet Mask | Total Available IP Addresses | Number of Usable Hosts |
| :---: | :--- | :---: | :---: |
| **`/30`** | `255.255.255.252` | `4` | `2` (Ideal for direct Point-to-Point Router links) |
| **`/28`** | `255.255.255.240` | `16` | `14` |
| **`/24`** | `255.255.255.0` | `256` | `254` |
| **`/16`** | `255.0.0.0` | `65,536` | `65,534` |

the reference picture you'll see inside the sub-folder netpractice/ is just an example of 1 of the 10 levels this project has. in order to pass this project you must configure and solve all the 10 levels  
---

## 🚀 Solved Scenarios Overview

The simulation environment tested networking logic across multiple complex levels:

1. **Simple Direct Links:** Configuring basic node-to-node interfaces on the same subnet where default gateways are not required.
2. **Switch Interconnections:** Establishing a unified Local Area Network (LAN) using a switch while managing conflicting host addresses.
3. **Multi-Subnet Routing:** Setting up standard routing paths where a local client must send data across a dual-interface router to reach an external web server.
4. **Internet Gateways & Mask Constraints:** Solving dense multi-level architecture schemas involving strict subnet sizing limitations and overlapping address parameters.

---

## 🛡️ Validation Rules Checked

Every network solution in this repository was systematically verified against the following core networking laws:
* The Network ID and Broadcast Address are never allocated to a host.
* Two host devices on the exact same local switch infrastructure **must** share the same subnet range.
* Two nodes located on different sides of a router **must** belong to entirely distinct network subnets.
* A router interface must always match the exact subnet scope of the host group it is physically servicing.
