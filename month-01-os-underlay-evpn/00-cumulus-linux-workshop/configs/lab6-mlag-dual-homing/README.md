# 🧪 Lab 02: MLAG Dual-Homing & L2 Redundancy


## 🎯 Objectives
- Configure Multi-Chassis Link Aggregation (MLAG) on Cumulus Linux switches using NVUE.
- Establish peer links, peer keepalives, and dual-homed bonds to hosts.
- Verify operational failover and active-active forwarding.

**Requirement**
Peerlink to be configured as LACP to carry the control traffic during normal operation and data traffic during outage
control plane operate over a dedicated vlan 4094 for MLAG operation
MLAG ID (1-65535) should be identical and essential for Bond to be recognised 
MAC address range dedicated for a pair of MLAG peer
MLAG backup IP ideally use the MGMT vrf alternatively you can use loopback IP addresses but needs routing or else a dedicated VRF 
Initialisation through a TCP session - primary and secondary based on priority