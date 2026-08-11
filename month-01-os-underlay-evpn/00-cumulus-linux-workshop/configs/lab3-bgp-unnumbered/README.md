## 📐 Topology Diagram

![Lab 01 Topology](topology.png)

**Quick Starter Checklist: Lab 01-bgp-unnumbered**

* Define switch hostnames, vlans, trunks, portBonds and loopbacks (nv set system hostname ...).
* Configure BGP Autonomous System numbers (nv set vrf default router bgp autonomous-system ...)[cite: 1, 2].
* Set up BGP Unnumbered interface peering (nv set vrf default router bgp neighbor <interface> remote-as external)[cite: 1, 2].
* Validate operational state (nv show vrf default router bgp neighbor) within 15 minutes[cite: 2].
* Export configuration to /labs/01-bgp-unnumbered/configs/[cite: 2].


# 🧪 Lab 01: BGP Unnumbered & Underlay Fabric

## Objectives
- Configure Cumulus Linux interfaces using NVUE CLI.
- Implement BGP Unnumbered using IPv6 Link-Local addressing across Spine-Leaf topologies[cite: 1].
- Verify BGP peering state and route propagation via `vtysh` and NVUE[cite: 1].

---

## Operational Constraints
* **Method**: Type commands manually in the CLI to build syntax muscle memory.

---

## Step-by-Step NVUE Commands

### 1. System & VRF Setup
```bash
# Set Hostname
nv set system hostname leaf01

# Enable BGP Autonomous System
nv set vrf default router bgp autonomous-system 65101
nv set vrf default router bgp router-id 10.0.0.1
