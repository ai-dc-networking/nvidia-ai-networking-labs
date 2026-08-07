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

## Verify Inter-VLAN Ping & VRR
* ping -c 3 10.0.10.1
* ping -c 3 10.0.20.1


# Lab 3: BGP Unnumbered and VRF-lite Configuration 

**Configure BGP Unnumbered**
* Advertise Loopback and SVI Subnets
* Quick Verify Connectivity with Servers

**VRF & Member Interfaces**
* VRF BGP Configuration
* Verify Routing Table
* Verify Connectivity

Appendix A: Enable SSH In Your Lab
