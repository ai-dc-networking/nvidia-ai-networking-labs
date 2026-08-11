** Lab 1: Verifying Lab Connectivity & Setup**
# Lab 2: Interface Configuration & Inter-VLAN Routing:

## Overview
This lab demonstrates core interface configuration, L2/L3 boundaries, VRR, and Inter-VLAN routing on Cumulus Linux using NVUE.

## Key Tasks Completed
* Hostname and Loopback address assignment
* Bond/LAG configuration for switch interconnects
* Bridge domain setup with Access/Trunk ports
* SVI creation with VRR (Virtual Router Redundancy)
* Inter-VLAN routing validation & MAC address learning verification

## Architecture & Topology
![Topology](./Topology/Topology%2001.JPG)

## Verification Highlights
* nv show system brief
* nv show interface lo link 
* nv show interface lo ipv4 address
* nv show interface bond0 bond
* nv show bridge domain br_default
* nv show interface swp1 bridge domain br_default
* nv show interface vlan10 ipv4 address  
* nv show interface vlan10 ipv4 vrr
* nv show bridge domain br_default mac
* nv show system date-time

# Verify Inter-VLAN routing & VRR
* ping -c 3 10.0.10.1
* ping -c 3 10.0.20.1


# Lab 3: BGP Unnumbered
**Configure BGP Unnumbered**
* Advertise Loopback and SVI Subnets
* Quick Verify Connectivity with Servers


# Lab 4: BGP-to-the-server 
This lab demonstrates extending the L3 Fabric control plane down to compute servers using eBGP Unnumbered (BGP-ttH). By running eBGP directly on host interfaces, servers participate dynamically in routing, providing ECMP load balancing and fast failover without requiring traditional L2 bridge/VLAN configurations or FHRP protocols

# Key Features
- Routing Protocol: eBGP Unnumbered over IPv6 Link-Local addresses
- Topology: Leaf-to-Server L3 Peering
- Traffic Model: Direct host prefix advertisement (`/32` loopback redistribution)


# Lab 5: BGP VRF-lite Configuration
**VRF & Member Interfaces**
* VRF BGP Configuration
* Verify Routing Table
* Verify Connectivity


# Lab 6: MLAG Dual Homing
Appendix A: Enable SSH In Your Lab