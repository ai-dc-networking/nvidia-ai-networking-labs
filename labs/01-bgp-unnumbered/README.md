# 🧪 Lab 01: BGP Unnumbered & Underlay Fabric

## 🎯 Objectives
- Configure Cumulus Linux interfaces using NVUE CLI.
- Implement BGP Unnumbered using IPv6 Link-Local addressing across Spine-Leaf topologies[cite: 1].
- Verify BGP peering state and route propagation via `vtysh` and NVUE[cite: 1].

---

## ⏱️ Operational Constraints
* **Execution Time**: Must complete configuration and validation within **15 minutes**.
* **Method**: Type commands manually in the CLI to build syntax muscle memory.

---

## 🛠️ Step-by-Step NVUE Commands

### 1. System & VRF Setup
```bash
# Set Hostname
nv set system hostname leaf01

# Enable BGP Autonomous System
nv set vrf default router bgp autonomous-system 65101
nv set vrf default router bgp router-id 10.0.0.1